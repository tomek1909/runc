load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library", "go_prefix")

go_library(
    name = "go_default_library",
    srcs = [
        "checkpoint.go",
        "create.go",
        "delete.go",
        "events.go",
        "exec.go",
        "kill.go",
        "list.go",
        "main.go",
        "main_unix.go",
        "pause.go",
        "ps.go",
        "restore.go",
        "rlimit_linux.go",
        "run.go",
        "signals.go",
        "spec.go",
        "start.go",
        "state.go",
        "tty.go",
        "update.go",
        "utils.go",
        "utils_linux.go",
    ],
    visibility = ["//visibility:private"],
    deps = [
        "@com_github_Sirupsen_logrus//:go_default_library",
        "@com_github_coreos_go_systemd//activation:go_default_library",
        "@com_github_docker_docker//pkg/term:go_default_library",
        "@com_github_docker_go_units//:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/cgroups:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/cgroups/systemd:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/configs:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/nsenter:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/specconv:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/system:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/utils:go_default_library",
        "@com_github_opencontainers_runtime_spec//specs-go:go_default_library",
        "@com_github_urfave_cli//:go_default_library",
    ],
)

go_binary(
    name = "runc",
    library = ":go_default_library",
    visibility = ["//visibility:public"],
)

