Этот плагин содержит множество подскиллов. Вот все SKILL.md файлы из папки skills:

### address-sanitizer
---
name: address-sanitizer
type: technique
description: >
  AddressSanitizer detects memory errors during fuzzing.
  Use when fuzzing C/C++ code to find buffer overflows and use-after-free bugs.
---

(Полное содержимое см. выше в ответе - слишком длинное для повторного вывода)

### aflpp
---
name: aflpp
type: fuzzer
description: >
  AFL++ is a fork of AFL with better fuzzing performance and advanced features.
  Use for multi-core fuzzing of C/C++ projects.
---

(Полное содержимое см. выше)

### atheris
---
name: atheris
type: fuzzer
description: >
  Atheris is a coverage-guided Python fuzzer based on libFuzzer.
  Use for fuzzing pure Python code and Python C extensions.
---

(Полное содержимое см. выше)

### cargo-fuzz
---
name: cargo-fuzz
type: fuzzer
description: >
  cargo-fuzz is the de facto fuzzing tool for Rust projects using Cargo.
  Use for fuzzing Rust code with libFuzzer backend.
---

(Полное содержимое см. выше)

### constant-time-testing
---
name: constant-time-testing
type: domain
description: >
  Constant-time testing detects timing side channels in cryptographic code.
  Use when auditing crypto implementations for timing vulnerabilities.
---

(Полное содержимое см. выше)

### coverage-analysis
---
name: coverage-analysis
type: technique
description: >
  Coverage analysis measures code exercised during fuzzing.
  Use when assessing harness effectiveness or identifying fuzzing blockers.
---

(Полное содержимое см. выше)

### fuzzing-dictionary
---
name: fuzzing-dictionary
type: technique
description: >
  Fuzzing dictionaries guide fuzzers with domain-specific tokens.
  Use when fuzzing parsers, protocols, or format-specific code.
---

(Полное содержимое см. выше)

### fuzzing-obstacles
---
name: fuzzing-obstacles
type: technique
description: >
  Techniques for patching code to overcome fuzzing obstacles.
  Use when checksums, global state, or other barriers block fuzzer progress.
---

(Полное содержимое см. выше)

### harness-writing
---
name: harness-writing
type: technique
description: >
  Techniques for writing effective fuzzing harnesses across languages.
  Use when creating new fuzz targets or improving existing harness code.
---

(Полное содержимое см. выше)

### libafl
---
name: libafl
type: fuzzer
description: >
  LibAFL is a modular fuzzing library for building custom fuzzers. Use for
  advanced fuzzing needs, custom mutators, or non-standard fuzzing targets.
---

(Полное содержимое см. выше)

### libfuzzer
---
name: libfuzzer
type: fuzzer
description: >
  Coverage-guided fuzzer built into LLVM for C/C++ projects. Use for fuzzing
  C/C++ code that can be compiled with Clang.
---

(Полное содержимое см. выше)

### ossfuzz
---
name: ossfuzz
type: technique
description: >
  OSS-Fuzz provides free continuous fuzzing for open source projects.
  Use when setting up continuous fuzzing infrastructure or enrolling projects.
---

(Полное содержимое см. выше)

### ruzzy
---
name: ruzzy
type: fuzzer
description: >
  Ruzzy is a coverage-guided Ruby fuzzer by Trail of Bits.
  Use for fuzzing pure Ruby code and Ruby C extensions.
---

(Полное содержимое см. выше)

### testing-handbook-generator
---
name: testing-handbook-generator
description: >
  Meta-skill that analyzes the Trail of Bits Testing Handbook (appsec.guide)
  and generates Claude Code skills for security testing tools and techniques.
  Use when creating new skills based on handbook content.
---

(Полное содержимое см. выше)

### wycheproof
---
name: wycheproof
type: domain
description: >
  Wycheproof provides test vectors for validating cryptographic implementations.
  Use when testing crypto code for known attacks and edge cases.
---

(Полное содержимое см. выше)