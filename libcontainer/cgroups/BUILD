load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "cgroups.go",
        "stats.go",
        "utils.go",
    ],
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_docker_go_units//:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/configs:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "cgroups_test.go",
        "utils_test.go",
    ],
    library = ":go_default_library",
)
