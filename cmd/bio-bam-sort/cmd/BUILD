load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["main.go"],
    importpath = "github.com/josh-newman/bio/cmd/bio-bam-sort/cmd",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_grailbio_base//file:go_default_library",
        "@com_github_grailbio_base//grail:go_default_library",
        "@com_github_grailbio_base//log:go_default_library",
        "@com_github_grailbio_base//vcontext:go_default_library",
        "@com_github_grailbio_hts//bam:go_default_library",
        "@com_github_grailbio_hts//sam:go_default_library",
    ],
)
