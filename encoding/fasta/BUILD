load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "fasta.go",
        "index.go",
    ],
    importpath = "github.com/josh-newman/bio/encoding/fasta",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_grailbio_base//errors:go_default_library",
        "@com_github_grailbio_base//tsv:go_default_library",
        "@com_github_pkg_errors//:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["fasta_test.go"],
    embed = [":go_default_library"],
    deps = [
        "@com_github_grailbio_base//file:go_default_library",
        "@com_github_grailbio_base//vcontext:go_default_library",
        "@com_github_grailbio_testutil//assert:go_default_library",
    ],
)
