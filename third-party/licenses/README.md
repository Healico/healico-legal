# Vendored third-party license texts

These files cover crates whose published package archive declares a license in `Cargo.toml` but omits the license text. Texts were fetched from the upstream repository at the commit recorded by Cargo's `.cargo_vcs_info.json` for the exact package version.

| Crate and version | Upstream source commit | Files |
| --- | --- | --- |
| `alloc-stdlib 0.2.2` | https://github.com/dropbox/rust-alloc-no-stdlib/tree/6032b6a9b20e03737135c55a0270ccffcc1438ef | `LICENSE` |
| `async-compression 0.4.35` | https://github.com/Nullus157/async-compression/tree/55741021c8d7b447a477d8bd7962a06b8a958315 | `LICENSE-APACHE`, `LICENSE-MIT` |
| `compression-codecs 0.4.34` | https://github.com/Nullus157/async-compression/tree/55741021c8d7b447a477d8bd7962a06b8a958315 | `LICENSE-APACHE`, `LICENSE-MIT` |
| `compression-core 0.4.31` | https://github.com/Nullus157/async-compression/tree/2a28343998e67ea519b87005b9d295b134c00dd0 | `LICENSE-APACHE`, `LICENSE-MIT` |
| `napi 2.16.17` | https://github.com/napi-rs/napi-rs/tree/f2178312d0e3e07beecc19836b91716a229107d3 | `LICENSE` |
| `napi-derive 2.16.13` | https://github.com/napi-rs/napi-rs/tree/a312b7eb4e12d3e0a3e9770429ee05c333947a39 | `LICENSE` |
| `napi-derive-backend 1.0.75` | https://github.com/napi-rs/napi-rs/tree/a312b7eb4e12d3e0a3e9770429ee05c333947a39 | `LICENSE` |
| `napi-sys 2.4.0` | https://github.com/napi-rs/napi-rs/tree/f1b8ab5e645e674df33c796ef75aa278cd1b4a31 | `LICENSE` |

Run `node scripts/generate-third-party-notices.cjs` after dependency changes. The generator combines these texts with license files already present in Cargo/OHPM package archives.

## 2026-09-17 发行构建补充

- `llvm-ohos-15.0.4/NOTICE`：当前 DevEco OpenHarmony Native SDK 的 `llvm/NOTICE` 原文，包含 libc++、libc++abi、libunwind 及 LLVM 例外和历史许可证。当前 HAP 的 `libc++_shared.so` 与 SDK `llvm/lib/aarch64-linux-ohos/libc++_shared.so` SHA-256 一致（`f69947af100b652e349ae51e4a4888bcc7a327db9085272d318176ef1782bf0f`）；编译器标识为 OHOS LLVM 15.0.4、commit `329916b990b43824d4b7e67de911fee7a966b1c8`。收录工具链通知不表示重新分发整个 SDK。
- `rust-std-1.93.0/`：已安装 Rust 1.93.0（commit `254b59607d4417e9dffbc307138ae5c86280fe4c`）的 `COPYRIGHT-library.html` 和 MIT/Apache-2.0 原文；保留标准库的例外及内嵌依赖通知。当前原生库的代码段与该工具链构建输出一致。升级工具链或替换原生库后必须重新核对。
- `brotli-8.0.2/LICENSE-BSD-dependency`：精确依赖 `brotli-decompressor 5.0.0` 包中的 `LICENSE`（Dropbox BSD-3-Clause），与 brotli 8.0.2 自带的 `LICENSE.MIT` 一起归档；完整来源区别见同目录 NOTICE。并非宣称找到了 brotli 仓库中不存在的根目录 BSD 许可证。两组件仍分别列示。


## OHPM 内嵌代码的本轮溯源结果

详见 [来源与复核记录](../provenance/README.md) 和固定证据 `../provenance/embedded.json`。

- `@ohos/jszip 1.0.1` 的 39 份 core/dist 文件逐一匹配 TPC 提交 `ebece08923c9400d104a9b2e1f4a42e0193c657f`。实际来源是 `xqdoo00o/jszip` 3.10.1 分支，不能标成原版 Stuk 3.5.0。JSZip 采用 MIT 选项，SJCL 采用 BSD 选项；保留原始双许可文本。
- 锁定的 Rollup 重建与实际 bundle 除一处外部模块导入尾斜杠外一致，证明可复现的依赖版本。它不是上游遗失的历史 lock，也不声称相同源码只能来自唯一 npm 版本。
- `@ohos/node-polyfill 1.0.1` 的 90 份 core/dist 文件匹配官方 `1.0.1` 标签提交 `cfaeb3882330768750c71b035d5bc9349b87bf45`。内嵌代码按适配后的提交和逐文件哈希标识，不把补充许可证的 npm 版本冒充历史内嵌版本；150 个命名 crypto 模块均映射到组件声明。原包 `README.OpenSource` 的 originjs 0.18.6 等版本说明未当作已验证标签。
- `embedded-js/` 保存各内嵌组件的完整许可证。来源 tarball 的地址、integrity 和 SHA-256 记录在证据中；`polyfill-snapshot/` 保留实际源码版权注释、原包 NOTICE、Apache 和 Mulan 许可。Google Closure 的 UTF-8 转换与 sha.js 的 BSD 部分单独保留，不能只写“全部 MIT”。
- `npm-license-sources.json` 和旧 `*-upstream` 补充材料保留作历史记录；当前生成器以 `embedded.json` 的组件和校验值为准。

## Rust 复合许可证

当前目标 normal/build 闭包的 136 个 crate 逐项登记在 `../provenance/rust-licenses.json`。已补充递归收录 `regex-syntax` 的 Unicode-DFS-2016、`ring` 的 once_cell/fiat、`tracing-core` 的 spin 许可证；保留相对路径，避免同名 LICENSE 被错误去重。`encoding_rs` 的 WHATWG、`unicode-ident` 的 Unicode-3.0、Brotli 的逐文件 MIT/BSD 范围分别保留。

`AND` 的各部分都保留；有明确 `OR` 的组件记录本次许可选择；Brotli 历史斜杠声明按实际文件处理，不机械转成二选一。LLVM 例外和 Rust 标准库内嵌声明仍完整交付。本次是当前锁定源码的核对，正式发行包及持续 LGPL 履约仍需后续完成。
