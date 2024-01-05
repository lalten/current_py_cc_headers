Demonstrate an issue with `@rules_python//python/cc:current_py_cc_headers`

https://github.com/bazelbuild/rules_python/issues/1669

```
❯ bazel test //...
ERROR: /home/runner/.cache/bazel/_bazel_runner/65a3e927bb675b9662534e6979f57f3e/external/rules_python/python/cc/BUILD.bazel:14:22: While resolving toolchains for target @@rules_python//python/cc:current_py_cc_headers (5b7f3da): No matching toolchains found for types @@rules_python//python/cc:toolchain_type.
To debug, rerun with --toolchain_resolution_debug='@@rules_python//python/cc:toolchain_type'
If platforms or toolchains are a new concept for you, we'd encourage reading https://bazel.build/concepts/platforms-intro.
ERROR: Analysis of target '//:test' failed; build aborted: Analysis failed
INFO: Elapsed time: 5.108s, Critical Path: 0.05s
INFO: 1 process: 1 internal.
ERROR: Build did NOT complete successfully
ERROR: No test targets were found, yet testing was requested
```
