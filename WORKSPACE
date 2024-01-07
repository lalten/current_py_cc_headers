load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_python",
    sha256 = "e85ae30de33625a63eca7fc40a94fea845e641888e52f32b6beea91e8b1b2793",
    strip_prefix = "rules_python-0.27.1",
    url = "https://github.com/bazelbuild/rules_python/archive/refs/tags/0.27.1.tar.gz",
)

load("@rules_python//python:repositories.bzl", "py_repositories", "python_register_toolchains")

py_repositories()

python_register_toolchains(
    name = "rules_ros2_python",
    python_version = "3.10",
)

# Workaround until https://github.com/bazelbuild/rules_python/pull/1670 is released
register_toolchains("@rules_ros2_python_toolchains//:x86_64-unknown-linux-gnu_py_cc_toolchain")
