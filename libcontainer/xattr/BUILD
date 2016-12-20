load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "errors.go",
        "xattr_linux.go",
    ],
    visibility = ["//visibility:public"],
    deps = ["//src/github.com/opencontainers/runc/libcontainer/system:go_default_library"],
)

go_test(
    name = "go_default_xtest",
    srcs = ["xattr_test.go"],
    deps = ["//src/github.com/opencontainers/runc/libcontainer/xattr:go_default_library"],
)
