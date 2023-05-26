# CapSanX

# Introduction

Traditional *CapSan* is developed by leveraging the convenience of [`__asan_*` public interface](https://github.com/llvm/llvm-project/blob/b5c862e15caf4d8aa34bbc6ee25af8da9a9405a4/compiler-rt/include/sanitizer/asan_interface.h#L263) provided by [AddressSanitizer](https://github.com/google/sanitizers/wiki/AddressSanitizer).
It links a piece of code called *bug-severity-rt.o* to target binary with the help of *afl-cc*.
So that a file which contains capability data can be saved when the target program crashes because of ASan-catchable errors. Later *CapFuzz* reads and utilizes this file.

However this workaround isn't easily scalable for other [sanitizers](https://github.com/google/sanitizers/wiki/) - not everyone has similar interfaces and headers available in compiler suite (either *LLVM* or *GNU GCC*), 
and the interfaces may be various across different versions.

Therefore *CapSanX* is proposed as the next generation, inspired by 
[*Custom Mutators in AFL++*](https://github.com/AFLplusplus/AFLplusplus/blob/4.06c/docs/custom_mutators.md).
It wrappers some Python modules to parse capability info from sanitizer reports, with rich and flexible text processing features available. *CapSanX* is going to be provided as a C-style library so that *CapFuzz* can benefit from it.

*CapSanX* is still under development (may be slow but hopeful).
