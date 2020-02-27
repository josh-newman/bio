load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["parsegencode.go"],
    importpath = "github.com/josh-newman/bio/fusion/parsegencode",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_grailbio_base//compress:go_default_library",
        "@com_github_grailbio_base//file:go_default_library",
        "@com_github_grailbio_base//log:go_default_library",
        "@com_github_grailbio_base//tsv:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["parsegencode_test.go"],
    data = glob(["testdata/**"]),
    embed = [":go_default_library"],
    deps = [
        "@com_github_grailbio_testutil//:go_default_library",
        "@com_github_grailbio_testutil//assert:go_default_library",
        "@com_github_grailbio_testutil//expect:go_default_library",
    ],
)
