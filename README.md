# Luna Kernel extra modules

本仓库管理 [Luna Kernel](https://github.com/LunaKernel/android_kernel_xiaomi_sm8850) 的额外用户态 KernelSU 模块模板，以 GPL-2.0 授权。

`ipset/` 包含 IPSet 模块的安装脚本、模块元数据与源码说明。它将用户态 `ipset` 命令安装到 `/system/bin/ipset`，需配合启用 IPSet 的内核使用。

本仓库不存放预编译二进制。主项目通过 `.env` 固定模板提交以及 IPSet、libmnl、Android NDK 来源，由 `init.sh` 准备依赖、`build.sh` 编译 Android arm64 命令并组装独立 KernelSU 模块 ZIP；二进制和上游许可证由主项目构建时填入。
