load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "disk_mate_shard.go",
        "distant_mate_table.go",
        "distant_mates.go",
        "doc.go",
        "mem_mate_shard.go",
        "shard_info.go",
    ],
    importpath = "github.com/josh-newman/bio/encoding/bampair",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_biogo_store//llrb:go_default_library",
        "@com_github_golang_snappy//:go_default_library",
        "@com_github_grailbio_base//log:go_default_library",
        "@com_github_grailbio_base//sync/multierror:go_default_library",
        "@com_github_grailbio_hts//bam:go_default_library",
        "@com_github_grailbio_hts//sam:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "distant_mates_test.go",
        "mate_shard_test.go",
        "shard_info_test.go",
    ],
    embed = [":go_default_library"],
    deps = [
        "@com_github_grailbio_base//grail:go_default_library",
        "@com_github_grailbio_hts//sam:go_default_library",
        "@com_github_grailbio_testutil//:go_default_library",
        "@com_github_stretchr_testify//assert:go_default_library",
    ],
)
