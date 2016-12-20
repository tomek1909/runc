load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "blkio_device.go",
        "cgroup_unix.go",
        "config.go",
        "config_unix.go",
        "device.go",
        "device_defaults.go",
        "hugepage_limit.go",
        "interface_priority_map.go",
        "mount.go",
        "namespaces.go",
        "namespaces_syscall.go",
        "namespaces_unix.go",
        "network.go",
    ],
    visibility = ["//visibility:public"],
    deps = ["@com_github_Sirupsen_logrus//:go_default_library"],
)

go_test(
    name = "go_default_test",
    srcs = ["config_unix_test.go"],
    library = ":go_default_library",
)

go_test(
    name = "go_default_xtest",
    srcs = ["config_test.go"],
    deps = ["//src/github.com/opencontainers/runc/libcontainer/configs:go_default_library"],
)
