load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "fragment.go",
        "fusion.go",
        "gene_db.go",
        "kmer.go",
        "kmer_index.go",
        "opts.go",
        "position.go",
        "postprocess.go",
        "preprocess.go",
        "stats.go",
        "stitcher.go",
        "util.go",
    ],
    importpath = "github.com/josh-newman/bio/fusion",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_dgryski_go_farm//:go_default_library",
        "@com_github_grailbio_base//file:go_default_library",
        "@com_github_grailbio_base//log:go_default_library",
        "@com_github_grailbio_base//simd:go_default_library",
        "@com_github_grailbio_base//tsv:go_default_library",
        "@com_github_grailbio_base//unsafe:go_default_library",
        "@com_github_minio_highwayhash//:go_default_library",
        "@org_golang_x_sys//unix:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "fragment_test.go",
        "fusion_test.go",
        "preprocess_test.go",
        "stitcher_test.go",
        "util_test.go",
    ],
    embed = [":go_default_library"],
    deps = [
        "@com_github_grailbio_testutil//:go_default_library",
        "@com_github_grailbio_testutil//assert:go_default_library",
        "@com_github_grailbio_testutil//expect:go_default_library",
        "@com_github_grailbio_testutil//h:go_default_library",
    ],
)
