# Healico 第三方软件声明（摘要）

更新日期：2026-09-17

本摘要列出随应用分发的主要第三方软件和许可证。完整许可证/声明原文已随应用包内置，也可在公网版本查看。

## LGPL-2.1 履约与三年书面要约

Healico 的 `libqrgen.so` 静态链接并分发 Libqrencode 4.1.1。Libqrencode 适用 LGPL-2.1-or-later。

1. 本声明随应用内置，明确告知每个副本使用了 Libqrencode 及其许可证；
2. 完整声明包含 LGPL-2.1 许可证原文；
3. 对应源代码和许可证见 https://github.com/ddyw/Healico/tree/store/entry/src/main/cpp/libqrencode，调用方源代码为 `entry/src/main/cpp/qrgen_napi.cpp`，构建链接配置为 `entry/src/main/cpp/CMakeLists.txt`；
4. 自本版本分发之日起至少三年内，接收方可发送邮件至 healico@foxmail.com，索取用于修改 Libqrencode 并重新链接生成修改版应用所需的对应机器可读源代码/目标代码材料；索取费用不超过复制和分发成本。

## 组件清单

本清单包含 Libqrencode、2 个随应用分发的 OHPM 组件、1 个开发测试组件，以及 Rust 构建闭包中的 136 个 crate。

| 组件 | 版本 | 许可证 | 来源/仓库 | 分发状态 | 许可证文件 |
| --- | --- | --- | --- | --- | --- |
| libqrencode | 4.1.1 | LGPL-2.1-or-later | https://github.com/fukuchi/libqrencode | 随应用分发 | COPYING |
| @hw-agconnect/auth | 1.0.5 | ISC | https://ohpm.openharmony.cn/#/cn/detail/%40hw-agconnect%2Fauth | 随应用分发 | LICENSE |
| @ohos/jszip | 1.0.1 | MIT | https://gitcode.com/openharmony-tpc/openharmony_tpc_samples/tree/master/ohos-jszip | 随应用分发 | LICENSE, NOTICE |
| @ohos/hypium | 1.0.21 | Apache-2.0 | https://gitee.com/openharmony/testfwk_arkxtest | 仅开发/测试 | LICENSE |
| adler2 | 2.0.1 | 0BSD OR MIT OR Apache-2.0 | https://github.com/oyvindln/adler2 | 随应用分发 | LICENSE-0BSD, LICENSE-APACHE, LICENSE-MIT |
| aho-corasick | 1.1.4 | Unlicense OR MIT | https://github.com/BurntSushi/aho-corasick | 随应用分发 | COPYING, LICENSE-MIT, UNLICENSE |
| alloc-no-stdlib | 2.0.4 | BSD-3-Clause | https://github.com/dropbox/rust-alloc-no-stdlib | 随应用分发 | LICENSE |
| alloc-stdlib | 0.2.2 | BSD-3-Clause | https://github.com/dropbox/rust-alloc-no-stdlib | 随应用分发 | LICENSE |
| async-compression | 0.4.35 | MIT OR Apache-2.0 | https://github.com/Nullus157/async-compression | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| atomic-waker | 1.1.2 | Apache-2.0 OR MIT | https://github.com/smol-rs/atomic-waker | 随应用分发 | LICENSE-APACHE, LICENSE-MIT, LICENSE-THIRD-PARTY |
| base64 | 0.22.1 | MIT OR Apache-2.0 | https://github.com/marshallpierce/rust-base64 | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| bitflags | 2.10.0 | MIT OR Apache-2.0 | https://github.com/bitflags/bitflags | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| brotli-decompressor | 5.0.0 | BSD-3-Clause/MIT | https://github.com/dropbox/rust-brotli-decompressor | 随应用分发 | LICENSE |
| brotli | 8.0.2 | BSD-3-Clause AND MIT | https://github.com/dropbox/rust-brotli | 随应用分发 | LICENSE.MIT |
| bytes | 1.11.0 | MIT | https://github.com/tokio-rs/bytes | 随应用分发 | LICENSE |
| cc | 1.2.49 | MIT OR Apache-2.0 | https://github.com/rust-lang/cc-rs | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| cfg-if | 1.0.4 | MIT OR Apache-2.0 | https://github.com/rust-lang/cfg-if | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| compression-codecs | 0.4.34 | MIT OR Apache-2.0 | https://github.com/Nullus157/async-compression | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| compression-core | 0.4.31 | MIT OR Apache-2.0 | https://github.com/Nullus157/async-compression | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| convert_case | 0.6.0 | MIT | https://github.com/rutrum/convert-case | 随应用分发 | LICENSE |
| cookie | 0.18.1 | MIT OR Apache-2.0 | https://github.com/SergioBenitez/cookie-rs | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| cookie_store | 0.21.1 | MIT OR Apache-2.0 | https://github.com/pfernie/cookie_store | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| crc32fast | 1.5.0 | MIT OR Apache-2.0 | https://github.com/srijs/rust-crc32fast | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| ctor | 0.2.9 | Apache-2.0 OR MIT | https://github.com/mmastrac/rust-ctor | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| deranged | 0.5.5 | MIT OR Apache-2.0 | https://github.com/jhpratt/deranged | 随应用分发 | LICENSE-APACHE, LICENSE-Apache, LICENSE-MIT |
| displaydoc | 0.2.5 | MIT OR Apache-2.0 | https://github.com/yaahc/displaydoc | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| document-features | 0.2.12 | MIT OR Apache-2.0 | https://github.com/slint-ui/document-features | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| encoding_rs | 0.8.35 | (Apache-2.0 OR MIT) AND BSD-3-Clause | https://github.com/hsivonen/encoding_rs | 随应用分发 | COPYRIGHT, LICENSE-APACHE, LICENSE-MIT, LICENSE-WHATWG |
| equivalent | 1.0.2 | Apache-2.0 OR MIT | https://github.com/indexmap-rs/equivalent | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| find-msvc-tools | 0.1.5 | MIT OR Apache-2.0 | https://github.com/rust-lang/cc-rs | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| flate2 | 1.1.5 | MIT OR Apache-2.0 | https://github.com/rust-lang/flate2-rs | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| fnv | 1.0.7 | Apache-2.0 / MIT | https://github.com/servo/rust-fnv | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| form_urlencoded | 1.2.2 | MIT OR Apache-2.0 | https://github.com/servo/rust-url | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| futures-channel | 0.3.31 | MIT OR Apache-2.0 | https://github.com/rust-lang/futures-rs | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| futures-core | 0.3.31 | MIT OR Apache-2.0 | https://github.com/rust-lang/futures-rs | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| futures-sink | 0.3.31 | MIT OR Apache-2.0 | https://github.com/rust-lang/futures-rs | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| futures-task | 0.3.31 | MIT OR Apache-2.0 | https://github.com/rust-lang/futures-rs | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| futures-util | 0.3.31 | MIT OR Apache-2.0 | https://github.com/rust-lang/futures-rs | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| getrandom | 0.2.16 | MIT OR Apache-2.0 | https://github.com/rust-random/getrandom | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| h2 | 0.4.12 | MIT | https://github.com/hyperium/h2 | 随应用分发 | LICENSE |
| hashbrown | 0.16.1 | MIT OR Apache-2.0 | https://github.com/rust-lang/hashbrown | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| http-body-util | 0.1.3 | MIT | https://github.com/hyperium/http-body | 随应用分发 | LICENSE |
| http-body | 1.0.1 | MIT | https://github.com/hyperium/http-body | 随应用分发 | LICENSE |
| http | 1.4.0 | MIT OR Apache-2.0 | https://github.com/hyperium/http | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| httparse | 1.10.1 | MIT OR Apache-2.0 | https://github.com/seanmonstar/httparse | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| hyper-rustls | 0.27.7 | Apache-2.0 OR ISC OR MIT | https://github.com/rustls/hyper-rustls | 随应用分发 | LICENSE, LICENSE-APACHE, LICENSE-ISC, LICENSE-MIT |
| hyper-util | 0.1.19 | MIT | https://github.com/hyperium/hyper-util | 随应用分发 | LICENSE |
| hyper | 1.8.1 | MIT | https://github.com/hyperium/hyper | 随应用分发 | LICENSE |
| icu_collections | 2.1.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| icu_locale_core | 2.1.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| icu_normalizer | 2.1.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| icu_normalizer_data | 2.1.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| icu_properties | 2.1.2 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| icu_properties_data | 2.1.2 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| icu_provider | 2.1.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| idna | 1.1.0 | MIT OR Apache-2.0 | https://github.com/servo/rust-url/ | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| idna_adapter | 1.2.1 | Apache-2.0 OR MIT | https://github.com/hsivonen/idna_adapter | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| indexmap | 2.12.1 | Apache-2.0 OR MIT | https://github.com/indexmap-rs/indexmap | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| ipnet | 2.11.0 | MIT OR Apache-2.0 | https://github.com/krisprice/ipnet | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| iri-string | 0.7.9 | MIT OR Apache-2.0 | https://github.com/lo48576/iri-string | 随应用分发 | LICENSE-APACHE.txt, LICENSE-MIT.txt |
| itoa | 1.0.15 | MIT OR Apache-2.0 | https://github.com/dtolnay/itoa | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| libc | 0.2.178 | MIT OR Apache-2.0 | https://github.com/rust-lang/libc | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| litemap | 0.8.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| litrs | 1.0.0 | MIT OR Apache-2.0 | https://github.com/LukasKalbertodt/litrs | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| log | 0.4.29 | MIT OR Apache-2.0 | https://github.com/rust-lang/log | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| memchr | 2.7.6 | Unlicense OR MIT | https://github.com/BurntSushi/memchr | 随应用分发 | COPYING, LICENSE-MIT, UNLICENSE |
| mime | 0.3.17 | MIT OR Apache-2.0 | https://github.com/hyperium/mime | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| miniz_oxide | 0.8.9 | MIT OR Zlib OR Apache-2.0 | https://github.com/Frommi/miniz_oxide/tree/master/miniz_oxide | 随应用分发 | LICENSE, LICENSE-APACHE.md, LICENSE-MIT.md, LICENSE-ZLIB.md |
| mio | 1.1.1 | MIT | https://github.com/tokio-rs/mio | 随应用分发 | LICENSE |
| napi-derive-backend | 1.0.75 | MIT | https://github.com/napi-rs/napi-rs | 随应用分发 | LICENSE |
| napi-derive | 2.16.13 | MIT | https://github.com/napi-rs/napi-rs | 随应用分发 | LICENSE |
| napi-sys | 2.4.0 | MIT | https://github.com/napi-rs/napi-rs | 随应用分发 | LICENSE |
| napi | 2.16.17 | MIT | https://github.com/napi-rs/napi-rs | 随应用分发 | LICENSE |
| num-conv | 0.1.0 | MIT OR Apache-2.0 | https://github.com/jhpratt/num-conv | 随应用分发 | LICENSE-APACHE, LICENSE-Apache, LICENSE-MIT |
| once_cell | 1.21.3 | MIT OR Apache-2.0 | https://github.com/matklad/once_cell | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| percent-encoding | 2.3.2 | MIT OR Apache-2.0 | https://github.com/servo/rust-url/ | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| pin-project-lite | 0.2.16 | Apache-2.0 OR MIT | https://github.com/taiki-e/pin-project-lite | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| pin-utils | 0.1.0 | MIT OR Apache-2.0 | https://github.com/rust-lang-nursery/pin-utils | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| potential_utf | 0.1.4 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| powerfmt | 0.2.0 | MIT OR Apache-2.0 | https://github.com/jhpratt/powerfmt | 随应用分发 | LICENSE-APACHE, LICENSE-Apache, LICENSE-MIT |
| proc-macro2 | 1.0.103 | MIT OR Apache-2.0 | https://github.com/dtolnay/proc-macro2 | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| psl-types | 2.0.11 | MIT/Apache-2.0 | https://github.com/addr-rs/psl-types | 随应用分发 | LICENSE, LICENSE-APACHE |
| publicsuffix | 2.3.0 | MIT/Apache-2.0 | https://github.com/rushmorem/publicsuffix | 随应用分发 | LICENSE, LICENSE-APACHE |
| quote | 1.0.42 | MIT OR Apache-2.0 | https://github.com/dtolnay/quote | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| regex-automata | 0.4.13 | MIT OR Apache-2.0 | https://github.com/rust-lang/regex | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| regex-syntax | 0.8.8 | MIT OR Apache-2.0 | https://github.com/rust-lang/regex | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| regex | 1.12.2 | MIT OR Apache-2.0 | https://github.com/rust-lang/regex | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| reqwest | 0.12.25 | MIT OR Apache-2.0 | https://github.com/seanmonstar/reqwest | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| ring | 0.17.14 | Apache-2.0 AND ISC | https://github.com/briansmith/ring | 随应用分发 | LICENSE, LICENSE-BoringSSL, LICENSE-other-bits |
| rustls-pki-types | 1.13.1 | MIT OR Apache-2.0 | https://github.com/rustls/pki-types | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| rustls-webpki | 0.103.8 | ISC | https://github.com/rustls/webpki | 随应用分发 | LICENSE |
| rustls | 0.23.35 | Apache-2.0 OR ISC OR MIT | https://github.com/rustls/rustls | 随应用分发 | LICENSE-APACHE, LICENSE-ISC, LICENSE-MIT |
| ryu | 1.0.20 | Apache-2.0 OR BSL-1.0 | https://github.com/dtolnay/ryu | 随应用分发 | LICENSE-APACHE, LICENSE-BOOST |
| semver | 1.0.28 | MIT OR Apache-2.0 | https://github.com/dtolnay/semver | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| serde | 1.0.228 | MIT OR Apache-2.0 | https://github.com/serde-rs/serde | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| serde_core | 1.0.228 | MIT OR Apache-2.0 | https://github.com/serde-rs/serde | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| serde_derive | 1.0.228 | MIT OR Apache-2.0 | https://github.com/serde-rs/serde | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| serde_json | 1.0.145 | MIT OR Apache-2.0 | https://github.com/serde-rs/json | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| serde_urlencoded | 0.7.1 | MIT/Apache-2.0 | https://github.com/nox/serde_urlencoded | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| shlex | 1.3.0 | MIT OR Apache-2.0 | https://github.com/comex/rust-shlex | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| simd-adler32 | 0.3.8 | MIT | https://github.com/mcountryman/simd-adler32 | 随应用分发 | LICENSE.md |
| slab | 0.4.11 | MIT | https://github.com/tokio-rs/slab | 随应用分发 | LICENSE |
| smallvec | 1.15.1 | MIT OR Apache-2.0 | https://github.com/servo/rust-smallvec | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| socket2 | 0.6.1 | MIT OR Apache-2.0 | https://github.com/rust-lang/socket2 | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| stable_deref_trait | 1.2.1 | MIT OR Apache-2.0 | https://github.com/storyyeller/stable_deref_trait | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| subtle | 2.6.1 | BSD-3-Clause | https://github.com/dalek-cryptography/subtle | 随应用分发 | LICENSE |
| syn | 2.0.111 | MIT OR Apache-2.0 | https://github.com/dtolnay/syn | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| sync_wrapper | 1.0.2 | Apache-2.0 | https://github.com/Actyx/sync_wrapper | 随应用分发 | LICENSE |
| synstructure | 0.13.2 | MIT | https://github.com/mystor/synstructure | 随应用分发 | LICENSE |
| time-core | 0.1.6 | MIT OR Apache-2.0 | https://github.com/time-rs/time | 随应用分发 | LICENSE-APACHE, LICENSE-Apache, LICENSE-MIT |
| time-macros | 0.2.24 | MIT OR Apache-2.0 | https://github.com/time-rs/time | 随应用分发 | LICENSE-APACHE, LICENSE-Apache, LICENSE-MIT |
| time | 0.3.44 | MIT OR Apache-2.0 | https://github.com/time-rs/time | 随应用分发 | LICENSE-APACHE, LICENSE-Apache, LICENSE-MIT |
| tinystr | 0.8.2 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| tokio-rustls | 0.26.4 | MIT OR Apache-2.0 | https://github.com/rustls/tokio-rustls | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| tokio-util | 0.7.17 | MIT | https://github.com/tokio-rs/tokio | 随应用分发 | LICENSE |
| tokio | 1.48.0 | MIT | https://github.com/tokio-rs/tokio | 随应用分发 | LICENSE |
| tower-http | 0.6.8 | MIT | https://github.com/tower-rs/tower-http | 随应用分发 | LICENSE |
| tower-layer | 0.3.3 | MIT | https://github.com/tower-rs/tower | 随应用分发 | LICENSE |
| tower-service | 0.3.3 | MIT | https://github.com/tower-rs/tower | 随应用分发 | LICENSE |
| tower | 0.5.2 | MIT | https://github.com/tower-rs/tower | 随应用分发 | LICENSE |
| tracing-core | 0.1.35 | MIT | https://github.com/tokio-rs/tracing | 随应用分发 | LICENSE |
| tracing | 0.1.43 | MIT | https://github.com/tokio-rs/tracing | 随应用分发 | LICENSE |
| try-lock | 0.2.5 | MIT | https://github.com/seanmonstar/try-lock | 随应用分发 | LICENSE |
| unicode-ident | 1.0.22 | (MIT OR Apache-2.0) AND Unicode-3.0 | https://github.com/dtolnay/unicode-ident | 随应用分发 | LICENSE-APACHE, LICENSE-MIT, LICENSE-UNICODE |
| unicode-segmentation | 1.13.3 | MIT OR Apache-2.0 | https://github.com/unicode-rs/unicode-segmentation | 随应用分发 | COPYRIGHT, LICENSE-APACHE, LICENSE-MIT |
| untrusted | 0.9.0 | ISC | https://github.com/briansmith/untrusted | 随应用分发 | LICENSE.txt |
| url | 2.5.7 | MIT OR Apache-2.0 | https://github.com/servo/rust-url | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| utf8_iter | 1.0.4 | Apache-2.0 OR MIT | https://github.com/hsivonen/utf8_iter | 随应用分发 | COPYRIGHT, LICENSE-APACHE, LICENSE-MIT |
| version_check | 0.9.5 | MIT/Apache-2.0 | https://github.com/SergioBenitez/version_check | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| want | 0.3.1 | MIT | https://github.com/seanmonstar/want | 随应用分发 | LICENSE |
| webpki-roots | 1.0.4 | CDLA-Permissive-2.0 | https://github.com/rustls/webpki-roots | 随应用分发 | LICENSE |
| writeable | 0.6.2 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| yoke-derive | 0.8.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| yoke | 0.8.1 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| zerofrom-derive | 0.1.6 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| zerofrom | 0.1.6 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| zeroize | 1.8.2 | Apache-2.0 OR MIT | https://github.com/RustCrypto/utils | 随应用分发 | LICENSE-APACHE, LICENSE-MIT |
| zerotrie | 0.2.3 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| zerovec-derive | 0.11.2 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |
| zerovec | 0.11.5 | Unicode-3.0 | https://github.com/unicode-org/icu4x | 随应用分发 | LICENSE |

## 完整许可证原文

完整组件清单、每个组件的许可证/NOTICE 原文和 SHA-256 校验值见应用包内 `THIRD_PARTY_NOTICES.md`，公网版本为 https://github.com/Healico/healico-legal/blob/main/THIRD_PARTY_NOTICES.md。

本摘要不减少开源许可证授予的权利；若摘要与许可证原文冲突，以许可证原文为准。

