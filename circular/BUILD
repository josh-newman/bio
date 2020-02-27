load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "bitmap.go",
        "circular.go",
        "doc.go",
    ],
    importpath = "github.com/josh-newman/bio/circular",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_grailbio_base//bitset:go_default_library",
        "@com_github_grailbio_base//log:go_default_library",
        "@com_github_grailbio_base//simd:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["bitmap_test.go"],
    embed = [":go_default_library"],
    deps = ["@com_github_grailbio_base//bitset:go_default_library"],
)
