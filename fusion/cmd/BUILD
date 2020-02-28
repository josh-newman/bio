load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "generate_transcriptome.go",
        "io.go",
        "main.go",
    ],
    importpath = "github.com/grailbio/bio/fusion/cmd",
    visibility = ["//visibility:public"],
    deps = [
        "//encoding/fasta:go_default_library",
        "//encoding/fastq:go_default_library",
        "//fusion:go_default_library",
        "//fusion/parsegencode:go_default_library",
        "@com_github_grailbio_base//compress:go_default_library",
        "@com_github_grailbio_base//errors:go_default_library",
        "@com_github_grailbio_base//file:go_default_library",
        "@com_github_grailbio_base//grail:go_default_library",
        "@com_github_grailbio_base//log:go_default_library",
        "@com_github_grailbio_base//recordio:go_default_library",
        "@com_github_grailbio_base//recordio/recordiozstd:go_default_library",
        "@com_github_grailbio_base//unsafe:go_default_library",
        "@com_github_grailbio_base//vcontext:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "fusion_e2e_test.go",
        "generate_transcriptome_e2e_test.go",
    ],
    embed = [":go_default_library"],
    deps = [
        "//encoding/fasta:go_default_library",
        "//fusion:go_default_library",
        "@com_github_grailbio_base//file:go_default_library",
        "@com_github_grailbio_base//grail:go_default_library",
        "@com_github_grailbio_base//log:go_default_library",
        "@com_github_grailbio_base//vcontext:go_default_library",
        "@com_github_grailbio_testutil//:go_default_library",
        "@com_github_grailbio_testutil//assert:go_default_library",
        "@com_github_grailbio_testutil//benchmark:go_default_library",
        "@com_github_grailbio_testutil//expect:go_default_library",
    ],
)
