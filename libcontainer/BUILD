load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "capabilities_linux.go",
        "capabilities_noambient.go",
        "console.go",
        "console_linux.go",
        "container.go",
        "container_linux.go",
        "criu_opts_unix.go",
        "error.go",
        "factory.go",
        "factory_linux.go",
        "generic_error.go",
        "init_linux.go",
        "message_linux.go",
        "network_linux.go",
        "notify_linux.go",
        "process.go",
        "process_linux.go",
        "restored_process.go",
        "rootfs_linux.go",
        "setgroups_linux.go",
        "setns_init_linux.go",
        "standard_init_linux.go",
        "state_linux.go",
        "stats.go",
        "stats_linux.go",
        "sync.go",
    ],
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_Sirupsen_logrus//:go_default_library",
        "@com_github_docker_docker//pkg/mount:go_default_library",
        "@com_github_docker_docker//pkg/symlink:go_default_library",
        "@com_github_golang_protobuf//proto:go_default_library",
        "@com_github_mrunalp_fileutils//:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/apparmor:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/cgroups:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/cgroups/fs:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/cgroups/systemd:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/configs:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/configs/validate:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/criurpc:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/keys:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/label:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/seccomp:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/stacktrace:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/system:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/user:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/utils:go_default_library",
        "@com_github_syndtr_gocapability//capability:go_default_library",
        "@com_github_vishvananda_netlink//:go_default_library",
        "@com_github_vishvananda_netlink//nl:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "container_linux_test.go",
        "error_test.go",
        "factory_linux_test.go",
        "generic_error_test.go",
        "notify_linux_test.go",
        "rootfs_linux_test.go",
        "state_linux_test.go",
    ],
    library = ":go_default_library",
    deps = [
        "@com_github_docker_docker//pkg/mount:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/cgroups:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/configs:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/utils:go_default_library",
    ],
)
