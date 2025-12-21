---
title: "🐞 测试"
weight: 3
cascade:
  type: docs
breadcrumbs: false
---

在构建之前, 请设置 -DENABLE_TEST=ON，默认是 OFF

```bash
cmake -B build -G Ninja -DCMAKE_BUILD_TYPE=Debug -DENABLE_TEST=ON
```

```txt
.
├── cases # <- 放置 ".test" 文件
│ ├── help.test
│ ├── list.test
│ ├── manual.test
│ ├── next.test
│ ├── previous.test
│ ├── refresh.test
│ ├── test.list
│ ├── unique-instance.test
│ └── version.test
├── CMakeLists.txt
├── fixtures
│ ├── config # <- 模拟目录 $XDG_RUNTIME_DIR/wow
│ └── workdir # <- 模拟目录 $XDG_CONFIG_HOME/wow
├── modify.sh
├── path.py.in
└── runtest.py # <- 回归测试脚本, 运行 ".test" 文件
```

{{< dino type="info" >}}
添加新的".test"文件后  
请重新执行`cmake --buiLd build`
{{< /dino >}}

- 运行所有测试

```bash
ctest --test-dir build --output-on-failure
```

- 单独运行测试

```bash
python3 test/runtest.py test/cases/[test name].test
```
