load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "lookup.go",
        "lookup_unix.go",
        "user.go",
    ],
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = ["user_test.go"],
    library = ":go_default_library",
    deps = ["//src/github.com/opencontainers/runc/libcontainer/utils:go_default_library"],
)
