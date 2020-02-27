load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "downsample.go",
        "scanner.go",
        "writer.go",
    ],
    importpath = "github.com/josh-newman/bio/encoding/fastq",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_grailbio_base//errors:go_default_library",
        "@com_github_grailbio_base//file:go_default_library",
        "@com_github_klauspost_compress//gzip:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "downsample_test.go",
        "scanner_test.go",
    ],
    data = glob(["testdata/**"]),
    embed = [":go_default_library"],
    deps = [
        "@com_github_grailbio_testutil//:go_default_library",
        "@com_github_grailbio_testutil//assert:go_default_library",
        "@com_github_grailbio_testutil//expect:go_default_library",
    ],
)
