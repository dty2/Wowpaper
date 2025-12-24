---
title: "🐞 Test"
weight: 3
cascade:
  type: docs
breadcrumbs: false
---

before build, please set "-DENABLE_TEST=ON", default is "OFF"

```bash
cmake -B build -G Ninja -DCMAKE_BUILD_TYPE=Debug -DENABLE_TEST=ON
```

```txt
.
├── cases  # <- put ".test" file
│   ├── help.test
│   ├── list.test
│   ├── manual.test
│   ├── next.test
│   ├── previous.test
│   ├── refresh.test
│   ├── test.list
│   ├── unique-instance.test
│   └── version.test
├── CMakeLists.txt
├── fixtures
│   ├── config  # <- simulation dir $XDG_RUNTIME_DIR/wow
│   └── workdir  # <- simulation dir $XDG_CONFIG_HOME/wow
├── modify.sh
├── path.py.in
└── runtest.py  # <- regression script , run ".test" file
```

{{< dino type="info" >}}
After adding a new ".test" file  
Please run `cmake --build build`
{{< /dino >}}

- run all test

```bash
ctest --test-dir build --output-on-failure
```

- run single test

```bash
python3 test/runtest.py test/cases/[test name].test
```
