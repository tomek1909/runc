load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["recvtty.go"],
    visibility = ["//visibility:private"],
    deps = [
        "//src/github.com/opencontainers/runc/libcontainer:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/utils:go_default_library",
        "@com_github_urfave_cli//:go_default_library",
    ],
)

go_binary(
    name = "recvtty",
    library = ":go_default_library",
    visibility = ["//visibility:public"],
)
