load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "pamreader.go",
        "pamwriter.go",
    ],
    importpath = "github.com/grailbio/bio/encoding/pam",
    visibility = ["//visibility:public"],
    deps = [
        "//biopb:go_default_library",
        "//encoding/bam:go_default_library",
        "//encoding/pam/fieldio:go_default_library",
        "//encoding/pam/pamutil:go_default_library",
        "@com_github_grailbio_base//errors:go_default_library",
        "@com_github_grailbio_base//file:go_default_library",
        "@com_github_grailbio_base//recordio/recordiozstd:go_default_library",
        "@com_github_grailbio_base//traverse:go_default_library",
        "@com_github_grailbio_base//vcontext:go_default_library",
        "@com_github_grailbio_hts//sam:go_default_library",
        "@io_v_x_lib//vlog:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["pam_e2e_test.go"],
    embed = [":go_default_library"],
    deps = [
        "//biopb:go_default_library",
        "//encoding/bam:go_default_library",
        "//encoding/bamprovider:go_default_library",
        "//encoding/converter:go_default_library",
        "//encoding/pam/pamutil:go_default_library",
        "@com_github_grailbio_base//grail:go_default_library",
        "@com_github_grailbio_base//traverse:go_default_library",
        "@com_github_grailbio_base//vcontext:go_default_library",
        "@com_github_grailbio_hts//bam:go_default_library",
        "@com_github_grailbio_hts//sam:go_default_library",
        "@com_github_grailbio_testutil//:go_default_library",
        "@com_github_grailbio_testutil//assert:go_default_library",
        "@com_github_grailbio_testutil//expect:go_default_library",
        "@io_v_x_lib//vlog:go_default_library",
    ],
)
