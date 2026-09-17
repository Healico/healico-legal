# Healico 第三方软件声明（摘要）

更新日期：2026-09-17

本摘要列出随应用分发的主要第三方软件和许可证。完整许可证/声明原文已随应用包内置，也可在公网版本查看。

## LGPL-2.1 履约与三年书面要约

Healico 的 `libqrgen.so` 静态链接并分发 Libqrencode 4.1.1。Libqrencode 适用 LGPL-2.1-or-later。

1. 本声明随应用内置，明确告知每个副本使用了 Libqrencode 及其许可证；
2. 完整声明包含 LGPL-2.1 许可证原文；
3. 对应版本的源代码、许可证、调用方目标文件、`qrgen_napi.cpp`、原 CMake 配置及重链接脚本见 https://github.com/Healico/healico-legal/tree/main/relink；无需访问私有仓库。包内 `src/libqrencode` 是实际编译源文件；
4. 自本版本分发之日起至少三年内，接收方可发送邮件至 healico@foxmail.com，索取用于修改 Libqrencode 并重新链接生成修改版应用所需的对应机器可读源代码/目标代码材料；索取费用不超过复制和分发成本。

允许接收者为自己的使用修改、重新链接，并为调试这些修改进行反向工程；本应用的其他条款不限制上述权利。

## 组件清单

本清单包含 Libqrencode、3 个随应用分发的 OHPM 组件、1 个开发测试组件、运行库与嵌入代码通知，以及 Rust 构建闭包中的 136 个 crate。上游许可证参考条目不代表已确定内嵌依赖的精确版本。

| 组件 | 版本 | 许可证 | 来源/仓库 | 分发状态 | 许可证文件 |
| --- | --- | --- | --- | --- | --- |
| libqrencode | 4.1.1 | LGPL-2.1-or-later | https://github.com/fukuchi/libqrencode | 分发或构建闭包 | COPYING |
| @hw-agconnect/auth | 1.0.5 | ISC | https://ohpm.openharmony.cn/#/cn/detail/%40hw-agconnect%2Fauth | 分发或构建闭包 | LICENSE |
| @ohos/jszip | 1.0.1 | MIT | https://gitcode.com/openharmony-tpc/openharmony_tpc_samples/tree/master/ohos-jszip | 分发或构建闭包 | LICENSE, NOTICE |
| @ohos/node-polyfill | 1.0.1 | Apache License 2.0 | https://gitcode.com/openharmony-sig/ohos_polyfill | 分发或构建闭包 | LICENSE, NOTICE |
| @ohos/hypium | 1.0.21 | Apache-2.0 | https://gitee.com/openharmony/testfwk_arkxtest | 仅开发/测试 | LICENSE |
| LLVM OHOS libc++ / libc++abi / libunwind | 15.0.4 | Apache-2.0 WITH LLVM-exception AND MIT AND NCSA | https://gitee.com/openharmony/third_party_llvm-project | 分发或构建闭包 | NOTICE |
| Rust standard library | 1.93.0 | MIT OR Apache-2.0 (with bundled third-party notices) | https://github.com/rust-lang/rust/tree/254b59607d4417e9dffbc307138ae5c86280fe4c | 分发或构建闭包 | COPYRIGHT-library.html, LICENSE-APACHE, LICENSE-MIT |
| JSZip upstream | 3.10.1 | MIT | https://github.com/Stuk/jszip/tree/v3.10.1 | 分发或构建闭包 | LICENSE.markdown |
| @ohos/jszip embedded notices | 1.0.1 bundle | MIT AND Zlib AND BSD-2-Clause (provenance review pending) | https://ohpm.openharmony.cn/#/cn/detail/%40ohos%2Fjszip | 分发或构建闭包 | NOTICE |
| lie upstream license reference | 3.3.0 | MIT | https://www.npmjs.com/package/lie/v/3.3.0 | 许可证参考；非版本认定 | license.md |
| immediate upstream license reference | 3.0.6 | MIT | https://www.npmjs.com/package/immediate/v/3.0.6 | 许可证参考；非版本认定 | LICENSE.txt |
| pako upstream license reference | 1.0.11 | MIT AND Zlib | https://www.npmjs.com/package/pako/v/1.0.11 | 许可证参考；非版本认定 | LICENSE, NOTICE-bundled-zlib |
| sjcl upstream license reference | 1.0.8 | BSD-2-Clause | https://www.npmjs.com/package/sjcl/v/1.0.8 | 许可证参考；非版本认定 | LICENSE.txt |
| adler2 | 2.0.1 | 0BSD OR MIT OR Apache-2.0 | https://github.com/oyvindln/adler2 | 分发或构建闭包 | LICENSE-0BSD, LICENSE-APACHE, LICENSE-MIT |
| aho-corasick | 1.1.4 | Unlicense OR MIT | https://github.com/BurntSushi/aho-corasick | 分发或构建闭包 | COPYING, LICENSE-MIT, UNLICENSE |
| alloc-no-stdlib | 2.0.4 | BSD-3-Clause | https://github.com/dropbox/rust-alloc-no-stdlib | 分发或构建闭包 | LICENSE |
| alloc-stdlib | 0.2.2 | BSD-3-Clause | https://github.com/dropbox/rust-alloc-no-stdlib | 分发或构建闭包 | LICENSE |
| async-compression | 0.4.35 | MIT OR Apache-2.0 | https://github.com/Nullus157/async-compression | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| atomic-waker | 1.1.2 | Apache-2.0 OR MIT | https://github.com/smol-rs/atomic-waker | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT, LICENSE-THIRD-PARTY |
| base64 | 0.22.1 | MIT OR Apache-2.0 | https://github.com/marshallpierce/rust-base64 | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| bitflags | 2.10.0 | MIT OR Apache-2.0 | https://github.com/bitflags/bitflags | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| brotli-decompressor | 5.0.0 | BSD-3-Clause/MIT | https://github.com/dropbox/rust-brotli-decompressor | 分发或构建闭包 | LICENSE |
| brotli | 8.0.2 | BSD-3-Clause AND MIT | https://github.com/dropbox/rust-brotli | 分发或构建闭包 | LICENSE.MIT, LICENSE-BSD-dependency, NOTICE |
| bytes | 1.11.0 | MIT | https://github.com/tokio-rs/bytes | 分发或构建闭包 | LICENSE |
| cc | 1.2.49 | MIT OR Apache-2.0 | https://github.com/rust-lang/cc-rs | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| cfg-if | 1.0.4 | MIT OR Apache-2.0 | https://github.com/rust-lang/cfg-if | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| compression-codecs | 0.4.34 | MIT OR Apache-2.0 | https://github.com/Nullus157/async-compression | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| compression-core | 0.4.31 | MIT OR Apache-2.0 | https://github.com/Nullus157/async-compression | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| convert_case | 0.6.0 | MIT | https://github.com/rutrum/convert-case | 分发或构建闭包 | LICENSE |
| cookie | 0.18.1 | MIT OR Apache-2.0 | https://github.com/SergioBenitez/cookie-rs | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| cookie_store | 0.21.1 | MIT OR Apache-2.0 | https://github.com/pfernie/cookie_store | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| crc32fast | 1.5.0 | MIT OR Apache-2.0 | https://github.com/srijs/rust-crc32fast | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| ctor | 0.2.9 | Apache-2.0 OR MIT | https://github.com/mmastrac/rust-ctor | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| deranged | 0.5.5 | MIT OR Apache-2.0 | https://github.com/jhpratt/deranged | 分发或构建闭包 | LICENSE-APACHE, LICENSE-Apache, LICENSE-MIT |
| displaydoc | 0.2.5 | MIT OR Apache-2.0 | https://github.com/yaahc/displaydoc | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| document-features | 0.2.12 | MIT OR Apache-2.0 | https://github.com/slint-ui/document-features | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| encoding_rs | 0.8.35 | (Apache-2.0 OR MIT) AND BSD-3-Clause | https://github.com/hsivonen/encoding_rs | 分发或构建闭包 | COPYRIGHT, LICENSE-APACHE, LICENSE-MIT, LICENSE-WHATWG |
| equivalent | 1.0.2 | Apache-2.0 OR MIT | https://github.com/indexmap-rs/equivalent | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| find-msvc-tools | 0.1.5 | MIT OR Apache-2.0 | https://github.com/rust-lang/cc-rs | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| flate2 | 1.1.5 | MIT OR Apache-2.0 | https://github.com/rust-lang/flate2-rs | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| fnv | 1.0.7 | Apache-2.0 / MIT | https://github.com/servo/rust-fnv | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| form_urlencoded | 1.2.2 | MIT OR Apache-2.0 | https://github.com/servo/rust-url | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| futures-channel | 0.3.31 | MIT OR Apache-2.0 | https://github.com/rust-lang/futures-rs | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| futures-core | 0.3.31 | MIT OR Apache-2.0 | https://github.com/rust-lang/futures-rs | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| futures-sink | 0.3.31 | MIT OR Apache-2.0 | https://github.com/rust-lang/futures-rs | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| futures-task | 0.3.31 | MIT OR Apache-2.0 | https://github.com/rust-lang/futures-rs | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| futures-util | 0.3.31 | MIT OR Apache-2.0 | https://github.com/rust-lang/futures-rs | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| getrandom | 0.2.16 | MIT OR Apache-2.0 | https://github.com/rust-random/getrandom | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| h2 | 0.4.12 | MIT | https://github.com/hyperium/h2 | 分发或构建闭包 | LICENSE |
| hashbrown | 0.16.1 | MIT OR Apache-2.0 | https://github.com/rust-lang/hashbrown | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| http-body-util | 0.1.3 | MIT | https://github.com/hyperium/http-body | 分发或构建闭包 | LICENSE |
| http-body | 1.0.1 | MIT | https://github.com/hyperium/http-body | 分发或构建闭包 | LICENSE |
| http | 1.4.0 | MIT OR Apache-2.0 | https://github.com/hyperium/http | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| httparse | 1.10.1 | MIT OR Apache-2.0 | https://github.com/seanmonstar/httparse | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| hyper-rustls | 0.27.7 | Apache-2.0 OR ISC OR MIT | https://github.com/rustls/hyper-rustls | 分发或构建闭包 | LICENSE, LICENSE-APACHE, LICENSE-ISC, LICENSE-MIT |
| hyper-util | 0.1.19 | MIT | https://github.com/hyperium/hyper-util | 分发或构建闭包 | LICENSE |
| hyper | 1.8.1 | MIT | https://github.com/hyperium/hyper | 分发或构建闭包 | LICENSE |
| icu_collections | 2.1.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| icu_locale_core | 2.1.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| icu_normalizer | 2.1.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| icu_normalizer_data | 2.1.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| icu_properties | 2.1.2 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| icu_properties_data | 2.1.2 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| icu_provider | 2.1.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| idna | 1.1.0 | MIT OR Apache-2.0 | https://github.com/servo/rust-url/ | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| idna_adapter | 1.2.1 | Apache-2.0 OR MIT | https://github.com/hsivonen/idna_adapter | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| indexmap | 2.12.1 | Apache-2.0 OR MIT | https://github.com/indexmap-rs/indexmap | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| ipnet | 2.11.0 | MIT OR Apache-2.0 | https://github.com/krisprice/ipnet | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| iri-string | 0.7.9 | MIT OR Apache-2.0 | https://github.com/lo48576/iri-string | 分发或构建闭包 | LICENSE-APACHE.txt, LICENSE-MIT.txt |
| itoa | 1.0.15 | MIT OR Apache-2.0 | https://github.com/dtolnay/itoa | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| libc | 0.2.178 | MIT OR Apache-2.0 | https://github.com/rust-lang/libc | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| litemap | 0.8.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| litrs | 1.0.0 | MIT OR Apache-2.0 | https://github.com/LukasKalbertodt/litrs | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| log | 0.4.29 | MIT OR Apache-2.0 | https://github.com/rust-lang/log | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| memchr | 2.7.6 | Unlicense OR MIT | https://github.com/BurntSushi/memchr | 分发或构建闭包 | COPYING, LICENSE-MIT, UNLICENSE |
| mime | 0.3.17 | MIT OR Apache-2.0 | https://github.com/hyperium/mime | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| miniz_oxide | 0.8.9 | MIT OR Zlib OR Apache-2.0 | https://github.com/Frommi/miniz_oxide/tree/master/miniz_oxide | 分发或构建闭包 | LICENSE, LICENSE-APACHE.md, LICENSE-MIT.md, LICENSE-ZLIB.md |
| mio | 1.1.1 | MIT | https://github.com/tokio-rs/mio | 分发或构建闭包 | LICENSE |
| napi-derive-backend | 1.0.75 | MIT | https://github.com/napi-rs/napi-rs | 分发或构建闭包 | LICENSE |
| napi-derive | 2.16.13 | MIT | https://github.com/napi-rs/napi-rs | 分发或构建闭包 | LICENSE |
| napi-sys | 2.4.0 | MIT | https://github.com/napi-rs/napi-rs | 分发或构建闭包 | LICENSE |
| napi | 2.16.17 | MIT | https://github.com/napi-rs/napi-rs | 分发或构建闭包 | LICENSE |
| num-conv | 0.1.0 | MIT OR Apache-2.0 | https://github.com/jhpratt/num-conv | 分发或构建闭包 | LICENSE-APACHE, LICENSE-Apache, LICENSE-MIT |
| once_cell | 1.21.3 | MIT OR Apache-2.0 | https://github.com/matklad/once_cell | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| percent-encoding | 2.3.2 | MIT OR Apache-2.0 | https://github.com/servo/rust-url/ | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| pin-project-lite | 0.2.16 | Apache-2.0 OR MIT | https://github.com/taiki-e/pin-project-lite | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| pin-utils | 0.1.0 | MIT OR Apache-2.0 | https://github.com/rust-lang-nursery/pin-utils | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| potential_utf | 0.1.4 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| powerfmt | 0.2.0 | MIT OR Apache-2.0 | https://github.com/jhpratt/powerfmt | 分发或构建闭包 | LICENSE-APACHE, LICENSE-Apache, LICENSE-MIT |
| proc-macro2 | 1.0.103 | MIT OR Apache-2.0 | https://github.com/dtolnay/proc-macro2 | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| psl-types | 2.0.11 | MIT/Apache-2.0 | https://github.com/addr-rs/psl-types | 分发或构建闭包 | LICENSE, LICENSE-APACHE |
| publicsuffix | 2.3.0 | MIT/Apache-2.0 | https://github.com/rushmorem/publicsuffix | 分发或构建闭包 | LICENSE, LICENSE-APACHE |
| quote | 1.0.42 | MIT OR Apache-2.0 | https://github.com/dtolnay/quote | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| regex-automata | 0.4.13 | MIT OR Apache-2.0 | https://github.com/rust-lang/regex | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| regex-syntax | 0.8.8 | MIT OR Apache-2.0 | https://github.com/rust-lang/regex | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| regex | 1.12.2 | MIT OR Apache-2.0 | https://github.com/rust-lang/regex | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| reqwest | 0.12.25 | MIT OR Apache-2.0 | https://github.com/seanmonstar/reqwest | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| ring | 0.17.14 | Apache-2.0 AND ISC | https://github.com/briansmith/ring | 分发或构建闭包 | LICENSE, LICENSE-BoringSSL, LICENSE-other-bits |
| rustls-pki-types | 1.13.1 | MIT OR Apache-2.0 | https://github.com/rustls/pki-types | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| rustls-webpki | 0.103.8 | ISC | https://github.com/rustls/webpki | 分发或构建闭包 | LICENSE |
| rustls | 0.23.35 | Apache-2.0 OR ISC OR MIT | https://github.com/rustls/rustls | 分发或构建闭包 | LICENSE-APACHE, LICENSE-ISC, LICENSE-MIT |
| ryu | 1.0.20 | Apache-2.0 OR BSL-1.0 | https://github.com/dtolnay/ryu | 分发或构建闭包 | LICENSE-APACHE, LICENSE-BOOST |
| semver | 1.0.28 | MIT OR Apache-2.0 | https://github.com/dtolnay/semver | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| serde | 1.0.228 | MIT OR Apache-2.0 | https://github.com/serde-rs/serde | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| serde_core | 1.0.228 | MIT OR Apache-2.0 | https://github.com/serde-rs/serde | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| serde_derive | 1.0.228 | MIT OR Apache-2.0 | https://github.com/serde-rs/serde | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| serde_json | 1.0.145 | MIT OR Apache-2.0 | https://github.com/serde-rs/json | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| serde_urlencoded | 0.7.1 | MIT/Apache-2.0 | https://github.com/nox/serde_urlencoded | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| shlex | 1.3.0 | MIT OR Apache-2.0 | https://github.com/comex/rust-shlex | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| simd-adler32 | 0.3.8 | MIT | https://github.com/mcountryman/simd-adler32 | 分发或构建闭包 | LICENSE.md |
| slab | 0.4.11 | MIT | https://github.com/tokio-rs/slab | 分发或构建闭包 | LICENSE |
| smallvec | 1.15.1 | MIT OR Apache-2.0 | https://github.com/servo/rust-smallvec | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| socket2 | 0.6.1 | MIT OR Apache-2.0 | https://github.com/rust-lang/socket2 | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| stable_deref_trait | 1.2.1 | MIT OR Apache-2.0 | https://github.com/storyyeller/stable_deref_trait | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| subtle | 2.6.1 | BSD-3-Clause | https://github.com/dalek-cryptography/subtle | 分发或构建闭包 | LICENSE |
| syn | 2.0.111 | MIT OR Apache-2.0 | https://github.com/dtolnay/syn | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| sync_wrapper | 1.0.2 | Apache-2.0 | https://github.com/Actyx/sync_wrapper | 分发或构建闭包 | LICENSE |
| synstructure | 0.13.2 | MIT | https://github.com/mystor/synstructure | 分发或构建闭包 | LICENSE |
| time-core | 0.1.6 | MIT OR Apache-2.0 | https://github.com/time-rs/time | 分发或构建闭包 | LICENSE-APACHE, LICENSE-Apache, LICENSE-MIT |
| time-macros | 0.2.24 | MIT OR Apache-2.0 | https://github.com/time-rs/time | 分发或构建闭包 | LICENSE-APACHE, LICENSE-Apache, LICENSE-MIT |
| time | 0.3.44 | MIT OR Apache-2.0 | https://github.com/time-rs/time | 分发或构建闭包 | LICENSE-APACHE, LICENSE-Apache, LICENSE-MIT |
| tinystr | 0.8.2 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| tokio-rustls | 0.26.4 | MIT OR Apache-2.0 | https://github.com/rustls/tokio-rustls | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| tokio-util | 0.7.17 | MIT | https://github.com/tokio-rs/tokio | 分发或构建闭包 | LICENSE |
| tokio | 1.48.0 | MIT | https://github.com/tokio-rs/tokio | 分发或构建闭包 | LICENSE |
| tower-http | 0.6.8 | MIT | https://github.com/tower-rs/tower-http | 分发或构建闭包 | LICENSE |
| tower-layer | 0.3.3 | MIT | https://github.com/tower-rs/tower | 分发或构建闭包 | LICENSE |
| tower-service | 0.3.3 | MIT | https://github.com/tower-rs/tower | 分发或构建闭包 | LICENSE |
| tower | 0.5.2 | MIT | https://github.com/tower-rs/tower | 分发或构建闭包 | LICENSE |
| tracing-core | 0.1.35 | MIT | https://github.com/tokio-rs/tracing | 分发或构建闭包 | LICENSE |
| tracing | 0.1.43 | MIT | https://github.com/tokio-rs/tracing | 分发或构建闭包 | LICENSE |
| try-lock | 0.2.5 | MIT | https://github.com/seanmonstar/try-lock | 分发或构建闭包 | LICENSE |
| unicode-ident | 1.0.22 | (MIT OR Apache-2.0) AND Unicode-3.0 | https://github.com/dtolnay/unicode-ident | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT, LICENSE-UNICODE |
| unicode-segmentation | 1.13.3 | MIT OR Apache-2.0 | https://github.com/unicode-rs/unicode-segmentation | 分发或构建闭包 | COPYRIGHT, LICENSE-APACHE, LICENSE-MIT |
| untrusted | 0.9.0 | ISC | https://github.com/briansmith/untrusted | 分发或构建闭包 | LICENSE.txt |
| url | 2.5.7 | MIT OR Apache-2.0 | https://github.com/servo/rust-url | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| utf8_iter | 1.0.4 | Apache-2.0 OR MIT | https://github.com/hsivonen/utf8_iter | 分发或构建闭包 | COPYRIGHT, LICENSE-APACHE, LICENSE-MIT |
| version_check | 0.9.5 | MIT/Apache-2.0 | https://github.com/SergioBenitez/version_check | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| want | 0.3.1 | MIT | https://github.com/seanmonstar/want | 分发或构建闭包 | LICENSE |
| webpki-roots | 1.0.4 | CDLA-Permissive-2.0 | https://github.com/rustls/webpki-roots | 分发或构建闭包 | LICENSE |
| writeable | 0.6.2 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| yoke-derive | 0.8.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| yoke | 0.8.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| zerofrom-derive | 0.1.6 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| zerofrom | 0.1.6 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| zeroize | 1.8.2 | Apache-2.0 OR MIT | https://github.com/RustCrypto/utils | 分发或构建闭包 | LICENSE-APACHE, LICENSE-MIT |
| zerotrie | 0.2.3 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| zerovec-derive | 0.11.2 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |
| zerovec | 0.11.5 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 分发或构建闭包 | LICENSE |

## 完整许可证原文

完整组件清单、每个组件的许可证/NOTICE 原文和 SHA-256 校验值见应用包内 `THIRD_PARTY_NOTICES.md`，公网版本为 https://github.com/Healico/healico-legal/blob/main/THIRD_PARTY_NOTICES.md。

本摘要不减少开源许可证授予的权利；若摘要与许可证原文冲突，以许可证原文为准。

