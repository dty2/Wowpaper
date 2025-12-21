---
title: "Build and Install"
cascade:
  type: docs
  params:
    reversePagination: false
breadcrumbs: false
---

- Dependence

{{< tabs items="Arch" >}}

{{< tab >}}

```bash
pacman -S pkgconf wayland wayland-protocols \
          wlr-protocols mesa ffmpeg \
          nlohmann-json tomlplusplus
```

{{< /tab >}}

{{< /tabs >}}

- Build Command

{{< tabs items="Release,Debug" >}}

{{< tab >}}

```bash
cmake -B build -G Ninja -DCMAKE_BUILD_TYPE=Release
```

{{< /tab >}}

{{< tab >}}

```bash
cmake -B build -G Ninja -DCMAKE_BUILD_TYPE=Debug
```

{{< /tab >}}

{{< /tabs >}}

```bash
cmake --build build
# Prefix needs to be specified
cmake --install build
```
