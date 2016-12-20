load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "apply_raw.go",
        "blkio.go",
        "cpu.go",
        "cpuacct.go",
        "cpuset.go",
        "devices.go",
        "freezer.go",
        "hugetlb.go",
        "memory.go",
        "name.go",
        "net_cls.go",
        "net_prio.go",
        "perf_event.go",
        "pids.go",
        "utils.go",
    ],
    visibility = ["//visibility:public"],
    deps = [
        "//src/github.com/opencontainers/runc/libcontainer/cgroups:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/configs:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/system:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/utils:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "apply_raw_test.go",
        "blkio_test.go",
        "cpu_test.go",
        "cpuset_test.go",
        "devices_test.go",
        "freezer_test.go",
        "hugetlb_test.go",
        "memory_test.go",
        "net_cls_test.go",
        "net_prio_test.go",
        "pids_test.go",
        "stats_util_test.go",
        "util_test.go",
        "utils_test.go",
    ],
    library = ":go_default_library",
    deps = [
        "@com_github_Sirupsen_logrus//:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/cgroups:go_default_library",
        "//src/github.com/opencontainers/runc/libcontainer/configs:go_default_library",
    ],
)
