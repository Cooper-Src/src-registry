# src-registry

> The official package registry for the **src** package manager.

`src-registry` contains community-maintained `.src` package manifests used by the `src` package manager. Each manifest describes how to obtain a package directly from its source repository.

---

## About

The registry serves as the central package index for the `src` ecosystem.

Unlike traditional package managers, the registry does **not** contain package source code—it only stores lightweight `.src` manifests that tell `src` where and how to obtain the original source.

---

## Repository Structure

```
packages/
    raylib.src
    glfw.src
    yaml-cpp.src
    fmt.src
```

Each file represents a single package.

---

## Example Manifest

```ini
name = raylib
version = 6.0
description = A simple and easy-to-use library to enjoy videogames programming

[source]
type = git
url = https://github.com/raysan5/raylib.git
branch = master

[license]
name = Zlib

[homepage]
url = https://www.raylib.com
```

---

## Using the Registry

Once configured, `src` can install packages directly from this registry.

```bash
src install raylib
```

Search for available packages:

```bash
src search ray
```

Update the local registry:

```bash
src registry update
```

---

## Contributing

Contributions are welcome!

To add a package:

1. Fork this repository.
2. Add your `.src` manifest to the `packages/` directory.
3. Verify the manifest is valid.
4. Submit a pull request.

Please ensure that:

- The package is open source.
- The source URL is official.
- The manifest is complete and correctly formatted.
- The package builds successfully from source.

---

## Related Projects

- **src** — The source-based package manager.
- **src-init** — Automatically generates `.src` manifests from GitHub repositories.

---

## License

This repository is licensed under the MIT License.
