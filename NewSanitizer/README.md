# The New Capability-Oriented Sanitizer

## Introduction

[Sanitizer](https://github.com/google/sanitizers) is our good buddy when running *Evocatio*. They enable us to access the capability data, no matter by report, C headers or flexible flags.

However those sanitizers, especially [AddressSanitizer](https://github.com/google/sanitizers/wiki/AddressSanitizer),
are *broad-spectrum*.
That is to say, once we enable them, the compiler suite will apply them *everywhere* possible rather than *somewhere*.
Although it may seem that we can provide a big [ignorelist](https://clang.llvm.org/docs/SanitizerSpecialCaseList.html#sanitizer-special-case-list), this has the two following drawbacks:
  - Finest granularity is function. We hope for fine-grained control such as Basic Block level.
  - It's *LLVM* suite limited. *GNU GCC* suite seems to have no corresponding thing.

Another keypoint is that, they provide so-called *capability* only when the target program has errors that they can detect. What about some capabilities beyond a traditional *CRASH*? Can we reuse the infrastructure behind those sanitizers to find some more generalized capabilities? Or maybe we can do capability mining with the help of a powerful debugger such as [LLDB](https://lldb.llvm.org/)?

Now it's time for some new *Capability-Oriented* sanitizers!
