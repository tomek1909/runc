load("@io_bazel_rules_go//go:def.bzl", "cgo_library", "go_library", "go_test")

cgo_library(
    name = "cgo_default_library",
    srcs = [
        "namespace.h",
        "nsenter.go",
        "nsexec.c",
    ],
    copts = ["-Wall"],
    visibility = ["//visibility:private"],
)

go_library(
    name = "go_default_library",
    library = ":cgo_default_library",
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = ["nsenter_test.go"],
    library = ":go_default_library",
    deps = [
        "//src/github.com/opencontainers/runc/libcontainer:go_default_library",
        "@com_github_vishvananda_netlink//nl:go_default_library",
    ],
)
