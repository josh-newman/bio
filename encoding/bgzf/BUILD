load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "writer.go",
        "writer_cgo.go",
        "writer_nocgo.go",
    ],
    importpath = "github.com/grailbio/bio/encoding/bgzf",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_grailbio_base//compress/libdeflate:go_default_library",
        "@com_github_yasushi_saito_zlibng//:go_default_library",
        "@io_v_x_lib//vlog:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["writer_test.go"],
    embed = [":go_default_library"],
    deps = [
        "@com_github_grailbio_base//grail:go_default_library",
        "@com_github_klauspost_compress//gzip:go_default_library",
        "@com_github_stretchr_testify//assert:go_default_library",
        "@com_github_stretchr_testify//require:go_default_library",
        "@com_github_yasushi_saito_zlibng//:go_default_library",
    ],
)
