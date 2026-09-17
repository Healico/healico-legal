# 第三方来源与许可证复核

复核日期：2026-09-17。范围为当前锁文件、安装的 OHPM 代码、Rust 目标构建闭包及已经识别的运行库。此记录不代表尚未生成的正式上架包已验收。

## 来源证据

| 对象 | 核定来源 | 验证方法 |
| --- | --- | --- |
| `@ohos/jszip 1.0.1` | [TPC 提交 ebece08923c9400d104a9b2e1f4a42e0193c657f](https://gitcode.com/openharmony-tpc/openharmony_tpc_samples/tree/ebece08923c9400d104a9b2e1f4a42e0193c657f/ohos-jszip/library) | 39 份 core/dist 文件逐一比较；只规范 CRLF，保留原始字节及 LF 两种 SHA-256 |
| JSZip 核心 | [xqdoo00o 提交 52378c05099c48bba49c2bbb4d9d549a3272d7a7](https://github.com/xqdoo00o/jszip/tree/52378c05099c48bba49c2bbb4d9d549a3272d7a7) | 自报 3.10.1；所有 lib 文件对应，只有 `sjcl.js` 的平台 crypto 获取方式存在已归档差异 |
| JSZip 子依赖 | `jszip-rebuild/package-lock.json` 中的可复现组合 | 从实际 core 源码重建；仅规范换行并修正一处 `string_decoder/` 外部导入尾斜杠，结果与已安装 bundle 全文相等 |
| `@ohos/node-polyfill 1.0.1` | [官方 1.0.1 标签对应的 cfaeb3882330768750c71b035d5bc9349b87bf45](https://gitcode.com/openharmony-sig/ohos_polyfill/tree/cfaeb3882330768750c71b035d5bc9349b87bf45/library) | 90 份 core/dist 文件逐一比较；150 个命名 crypto 模块全部对应到组件许可证条目 |
| Rust 136 个 crate | `Cargo.lock`、目标 normal/build 图、已校验的 crates.io 归档和包内源码提交 | `rust-licenses.json` 固定版本、归档 SHA-256、许可选择及递归许可证文件哈希 |

JSZip 的重建锁是**本次验证产生的锁**，不伪装成上游历史锁。能重建出相同源码不表示只能来自唯一历史 npm 版本。node-polyfill 中经过改写、合并的子组件采用**准确的适配源码快照**作为版本标识；`licenseReference.version` 只说明补充许可证文本取自哪个 npm 包，不能读成历史内嵌版本。原包中 JSZip 3.5.0、originjs 0.18.6 等旧描述原样保留，但不作为本次版本结论。

`embedded.json` 含上游路径、固定提交、129 份文件的校验值、模块与许可证映射以及 npm 许可证来源和 integrity。npm 补充材料下载时经过 integrity 校验。应用依赖本身没有替换、升级或删除密码/加密能力。

## 条款处理

| 对象 | 本次处理 |
| --- | --- |
| JSZip / SJCL | 分别选 MIT / BSD-2-Clause；保留原始双许可文本和实际版权声明，不要求把 App 改成 GPL |
| pako / sha.js | 分别保留 MIT + Zlib、MIT + BSD-3-Clause，不能把 `AND` 简化成选一项 |
| node-polyfill | 保留原包 Apache/NOTICE、实际源文件署名及相关 MIT/ISC/BSD、Mulan 文本；hash.js 引用的 Google Closure UTF-8 代码另保留 Apache 许可与版权 |
| encoding_rs | 代码选 MIT，WHATWG 数据的 BSD 和 COPYRIGHT 仍需保留 |
| unicode-ident / regex-syntax | 前者保留 Unicode-3.0，后者实际嵌套文本为 Unicode-DFS-2016；不得统一套用新版 Unicode 文本 |
| brotli / brotli-decompressor | 编码器 MIT、解码器根目录 Dropbox BSD，以及源码中 Google MIT 分别保留；解码器旧斜杠声明不机械视作二选一。编码器的 BSD 补充明确来自对应解码依赖，未伪造不存在的上游文件 |
| ring | Apache + ISC 按原文件范围保留；once_cell 选 MIT，fiat 与 BoringSSL 许可及源文件版权注释另收录 |
| tracing-core | 根目录 MIT 与 `src/spin/LICENSE` 的独立作者声明均保留 |
| LLVM / Rust 标准库 | LLVM Apache 例外、历史 MIT/NCSA，以及 Rust 标准库完整内嵌版权声明继续交付；不能仅用主许可证替代 |
| webpki-roots | 保留 CDLA-Permissive-2.0 数据许可，不凭它给 App 输出附加新的限制 |

每个 Rust 条目的 `declaredLicense` 保持上游原声明，`selectedLicense` 记录本次选择或保守同时履行的条款，`evidence` 解释适用范围。摘要不修改上游许可，也不将归属不同文件的许可强行套到整个应用。

本轮没有修改第三方运行时代码。今后修改 Apache/Zlib 等来源时，需保留通知并按相应条款标注改动；商标和署名不得用来暗示上游背书。

## 重复验证

在项目根目录运行：

```sh
node scripts/third-party-evidence.cjs
node scripts/generate-third-party-notices.cjs
node scripts/run-regressions.cjs
```

证据校验和声明生成器不会自动刷新“已审核”哈希。依赖锁、源码文件集合/内容或许可证改变会报错；须先审查差异、补足材料，再人工更新固定记录。递归收录时保留相对路径，不能按 `LICENSE` 文件名去重。

独立检验固定上游提交（克隆的仓库必须包含所列提交）：

```sh
node scripts/third-party-evidence.cjs --upstream jszip /path/to/openharmony_tpc_samples
node scripts/third-party-evidence.cjs --upstream node-polyfill /path/to/ohos_polyfill
```

重放 JSZip 构建需要网络取得锁定 npm 依赖；命令只在临时目录构建，不修改 App 已安装依赖，并禁用 npm 生命周期脚本：

```sh
node scripts/rebuild-third-party-jszip.cjs
```

## 后续边界

前两类整改针对本次锁定源码与声明完成。正式 release/市场处理后包仍须重新核对实际库、资源、调试信息、许可证可达性及 LGPL 重链接材料是否匹配；用户尚无上架包，本轮不声称已完成。历史交付包不得覆盖，至少三年书面要约需持续履行。
