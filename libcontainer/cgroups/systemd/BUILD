load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["apply_systemd.go"],
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_coreos_go_systemd//dbus:go_default_library",
        "@com_github_coreos_go_systemd//util:go_default_library",
        "@com_github_godbus_dbus//:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/cgroups:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/cgroups/fs:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/configs:go_default_library",
    ],
)
