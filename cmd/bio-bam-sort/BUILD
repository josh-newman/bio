load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["main.go"],
    importpath = "github.com/grailbio/bio/cmd/bio-bam-sort",
    visibility = ["//visibility:private"],
    deps = ["//cmd/bio-bam-sort/cmd:go_default_library"],
)

go_binary(
    name = "bio-bam-sort",
    embed = [":go_default_library"],
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = ["main_test.go"],
    embed = [":go_default_library"],
    deps = [
        "@com_github_grailbio_testutil//:go_default_library",
        "@com_github_stretchr_testify//require:go_default_library",
        "@io_v_x_lib//gosh:go_default_library",
    ],
)
