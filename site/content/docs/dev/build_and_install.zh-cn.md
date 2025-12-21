---
title: "构建与安装"
cascade:
  type: docs
  params:
    reversePagination: false
breadcrumbs: false
---

- 依赖库

{{< tabs items="Arch" >}}

{{< tab >}}

```bash
pacman -S pkgconf wayland wayland-protocols \
          wlr-protocols mesa ffmpeg \
          nlohmann-json tomlplusplus
```

{{< /tab >}}

{{< /tabs >}}

- 构建命令

```bash
# release
cmake -B build -G Ninja -DCMAKE_BUILD_TYPE=Release
# debug
cmake -B build -G Ninja -DCMAKE_BUILD_TYPE=Debug

cmake --build build
# 需要指定安装前缀
cmake --install build
```
