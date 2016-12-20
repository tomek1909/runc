load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["spec_linux.go"],
    visibility = ["//visibility:public"],
    deps = [
        "//src/github.com/opencontainers/runc/libcontainer/configs:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/seccomp:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/utils:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["spec_linux_test.go"],
    library = ":go_default_library",
    deps = ["@com_github_opencontainers_runtime_spec//specs-go:go_default_library"],
)
