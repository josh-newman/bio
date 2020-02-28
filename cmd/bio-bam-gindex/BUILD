load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "main.go",
    ],
    importpath = "github.com/grailbio/bio/cmd/bio-bam-gindex",
    visibility = ["//visibility:private"],
    deps = [
        "//encoding/bam:go_default_library",
        "@com_github_grailbio_base//grail:go_default_library",
    ],
)

go_binary(
    name = "bio-bam-gindex",
    embed = [":go_default_library"],
    visibility = ["//visibility:public"],
)
