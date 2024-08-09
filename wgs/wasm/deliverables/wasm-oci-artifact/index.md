---
title: Wasm OCI Artifact layout
---

# Wasm OCI Artifact layout

This is a guide for an [OCI image format](https://github.com/opencontainers/image-spec/tree/main) for Wasm that can be used across projects in order to enable consistency for users, tooling and registries. 
This OCI artifact has a specific Wasm `config.mediaType` of `application/vnd.wasm.config.v0+json` to designate it as an [OCI artifact](https://github.com/opencontainers/image-spec/blob/main/artifacts-guidance.md). 
It contains a representation of Wasm configuration that can be broadly be used across projects (various Wasm runtimes and container runtimes). 
It includes the ability to include wasm modules or components in the artifact.

It is designed to be compliant with the artifact guidance of the [OCI image spec](https://github.com/opencontainers/image-spec/blob/main/manifest.md#guidelines-for-artifact-usage) 
in order to be compatible with the widest range of registries today.
  
### Goals

- Single OCI compliant artifact type that can be used across container runtimes and Wasm runtime projects (wasmcloud, spin, containerd, podman, etc)
- Single layer type that is supported where everything is a component, which makes it so all the tools don’t need to know about all possible layer types (eg. static files, Wasm runtime config files, etc.).  
- Should be able to support an “exploded” representation of the component where each component is a layer and can be combined (“composed”) by either Wasm runtime or container runtime
- Have fall back if registries don’t support artifacts (via config.media type)

### Non Goals

- Support for use in browsers.  As use cases are presented we may reconsider.

## Manifest format

The Wasm `config.mediaType` configuration allows for easy identification of a Wasm artifact in a registry. See the `config.mediaType` section below for more details on the format of the config file. 

A single layer `mediaType` of `application/wasm` was chosen since a component can be both a library and an executable and so we don't want to need to indicate a difference between components. In addition, a component can always be recomposed into a another type. Although out of scope this does allow for potential browser support in future since browser only supports `application/wasm`.

```jsonc
{
    "schemaVersion": 2,
    "mediaType": "application/vnd.oci.image.manifest.v1+json",
    "annotations": {
        "anything": "you-want-per-spec"
    },
    "config": {
        // v0 the first version of the spec, but does not imply instability
        "mediaType": "application/vnd.wasm.config.v0+json",
        "size": 78,
        "digest": "sha256:1234567890"
    },
    "layers": [
        // Index 0 of the layers is the entrypoint to the application. As we start using this, it is most likely that you’ll just have a single layer consisting of the composed component. 
        // However, this is explicitly called out as we expect to be storing "exploded" components in order to reuse/share layers. 
        // When exploded components are stored as layers, they MUST use content hash importing, but this is not officially part of this spec yet. 
        // If a consumer sees more than a single layer for this version of the spec, they should reject it 
        {
            "mediaType": "application/wasm",
            "size": 146992,
            "digest": "sha256:1234567890"
        },
        {
            "mediaType": "application/wasm",
            "size": 692031,
            "digest": "sha256:1234567890"
        },
    ]
}
```

## Config.mediaType (`application/vnd.wasm.config.v0+json`)

The configuration provides the ability to quickly identify imports, exports or worlds that are used by the component. By specifying imports and exports, 
it ensures a runtime can validate that the component has all of the layers required to satisfy the exports. It also ensures that a Wasm runtime can reject 
running the a component if it can not satisfy the imports.

```jsonc
{
    "created": "2015-10-31T22:22:56.015925234Z",
    // This can be set here or as an annotation
    "author": "Alyssa P. Hacker <alyspdev@example.com>",
    "architecture": "wasm",
    // Eventually this will go away when we hit a 1.0 but we need it for now
    // Possible options: wasip1, wasip2. For plain wasm, this should be wasip1 as this must match a GOOS value and it doesn’t have one for plain Wasm
    "os": "wasip2",
    // We need to have a unique list here so that the hash of the config (used as the ID) is unique every time (https://github.com/opencontainers/image-spec/pull/1173). These are just the digests of the layers in the same order
    "layerDigests": [
        "sha256:123456",
        "sha256:abcdef"
    ],
    // This field MUST be present when it is a component (wasip2)
    "component": {
        // Decision: Optional imports will be a thing in the future, so when that happens we will add an additional field called "optional_imports"
        "exports": [
            "wasi:http/incoming-handler@0.2.0",
            "function-name"
        ],
        "imports": [
            "wasi:filesystem/types@0.2.0",
            "function-name"
        ],
        // This is optional metadata for indexing. Implementations MAY use this information to fetch other data to inspect the specified world
        "target": "wasi:http/proxy@0.2.0",
    },
    // In the future, we could add an optional "module" section that is only present when the OS value is wasip1. This could carry additional config data or other options. 
    // However, we are not adding this to start but would be more than willing to add it in as concrete use cases emerge. For components, config and other data will be
    // handled via composition using tools like wasi-virt
}
```

## FAQ

#### If there is a single layer type how will static files or runtime configuration files be supplied?

- Runtime configuration: WASI spec like  https://github.com/WebAssembly/wasi-runtime-config/pull/4 or specialized component that the host runtime would require 
- Static files: Virtual file system - https://github.com/bytecodealliance/wasi-virt?tab=readme-ov-file#filesystem or specialized component that could be provided to do further customization

## Implementations

**Implemented**

- cargo-component
- containerd
- wasmCloud
- wasm-pkg-tools (wkg)

**Interested**

- componentize-dotnet
- Spin

If your project has implemented this as well or is interested, please open a PR to add it to the list!

## Prior Discussions

Working group notes: https://docs.google.com/document/d/1pVqmU5-zs2IZAg9oV01wH0wZaHYotuI5CA0777h-O0Y
Original Design document: https://docs.google.com/document/d/1bZLjDpcG22PruvSUxGH-DNL906GEV0fYIbHQH7eNzqs
Presentations to wg-wasm: https://youtu.be/YrdjQ7NEGqI?t=541

# Contributors

- Taylor Thomas
- Luke Wagner
- Calvin Prewitt
- Brandon Mitchell
- James Sturtevant
- Lann Martin
