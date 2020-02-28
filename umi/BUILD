load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["correction.go"],
    importpath = "github.com/grailbio/bio/umi",
    visibility = ["//visibility:public"],
    deps = [
        "//util:go_default_library",
        "@com_github_grailbio_base//log:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["correction_test.go"],
    embed = [":go_default_library"],
    deps = [
        "@com_github_grailbio_base//grail:go_default_library",
        "@com_github_stretchr_testify//assert:go_default_library",
    ],
)
