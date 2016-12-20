load("@io_bazel_rules_go//go:def.bzl", "cgo_library", "go_library", "go_test")

cgo_library(
    name = "cgo_default_library",
    srcs = ["sysconfig.go"],
    visibility = ["//visibility:private"],
)

go_library(
    name = "go_default_library",
    srcs = [
        "linux.go",
        "proc.go",
        "setns_linux.go",
        "syscall_linux_64.go",
        "xattrs_linux.go",
    ],
    library = ":cgo_default_library",
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = ["proc_test.go"],
    library = ":go_default_library",
)
