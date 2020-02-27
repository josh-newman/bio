load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["process_example.go"],
    importpath = "github.com/josh-newman/bio/encoding/bam/process_example",
    visibility = ["//visibility:private"],
    deps = [
        "@com_github_grailbio_base//grail:go_default_library",
        "@com_github_grailbio_hts//sam:go_default_library",
        "@io_v_x_lib//vlog:go_default_library",
    ],
)

go_binary(
    name = "process_example",
    embed = [":go_default_library"],
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = ["benchmark_test.go"],
    data = glob(["testdata/**"]),
    embed = [":go_default_library"],
)
