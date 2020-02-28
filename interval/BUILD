load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "bedunion.go",
        "doc.go",
        "endpoint_index.go",
    ],
    importpath = "github.com/grailbio/bio/interval",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_grailbio_base//file:go_default_library",
        "@com_github_grailbio_base//fileio:go_default_library",
        "@com_github_grailbio_base//log:go_default_library",
        "@com_github_grailbio_base//unsafe:go_default_library",
        "@com_github_grailbio_base//vcontext:go_default_library",
        "@com_github_grailbio_hts//sam:go_default_library",
        "@com_github_klauspost_compress//gzip:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["bedunion_internal_test.go"],
    data = glob(["testdata/**"]),
    embed = [":go_default_library"],
    deps = [
        "@com_github_grailbio_hts//sam:go_default_library",
        "@com_github_grailbio_testutil//expect:go_default_library",
    ],
)
