load("@io_bazel_rules_go//go:def.bzl", "cgo_library", "go_library", "go_test")

cgo_library(
    name = "cgo_default_library",
    srcs = [
        "cmsg.c",
        "cmsg.go",
        "cmsg.h",
    ],
    visibility = ["//visibility:private"],
)

go_library(
    name = "go_default_library",
    srcs = [
        "utils.go",
        "utils_unix.go",
    ],
    library = ":cgo_default_library",
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = ["utils_test.go"],
    library = ":go_default_library",
)
