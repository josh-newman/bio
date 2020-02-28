load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "file_info.go",
        "index.go",
        "pamutil.go",
        "sharder.go",
    ],
    importpath = "github.com/grailbio/bio/encoding/pam/pamutil",
    visibility = ["//visibility:public"],
    deps = [
        "//biopb:go_default_library",
        "//encoding/bam:go_default_library",
        "@com_github_grailbio_base//errors:go_default_library",
        "@com_github_grailbio_base//file:go_default_library",
        "@com_github_grailbio_base//log:go_default_library",
        "@com_github_grailbio_base//recordio:go_default_library",
        "@com_github_grailbio_base//vcontext:go_default_library",
        "@com_github_grailbio_hts//bam:go_default_library",
        "@com_github_grailbio_hts//sam:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["pamutil_test.go"],
    embed = [":go_default_library"],
    deps = [
        "//biopb:go_default_library",
        "//encoding/bam:go_default_library",
        "@com_github_grailbio_testutil//expect:go_default_library",
    ],
)
