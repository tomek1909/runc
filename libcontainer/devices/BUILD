load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "devices_unix.go",
        "number.go",
    ],
    visibility = ["//visibility:public"],
    deps = ["//src/github.com/opencontainers/runc/libcontainer/configs:go_default_library"],
)

go_test(
    name = "go_default_test",
    srcs = ["devices_test.go"],
    library = ":go_default_library",
)
