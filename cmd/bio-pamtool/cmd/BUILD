load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "checksum.go",
        "filter.go",
        "flagstat.go",
        "main.go",
        "view.go",
    ],
    importpath = "github.com/grailbio/bio/cmd/bio-pamtool/cmd",
    visibility = ["//visibility:public"],
    deps = [
        "//encoding/bam:go_default_library",
        "//encoding/bamprovider:go_default_library",
        "//encoding/converter:go_default_library",
        "//encoding/pam:go_default_library",
        "@com_blainsmith_go_seahash//:go_default_library",
        "@com_github_grailbio_base//cmdutil:go_default_library",
        "@com_github_grailbio_base//errors:go_default_library",
        "@com_github_grailbio_base//log:go_default_library",
        "@com_github_grailbio_base//syncqueue:go_default_library",
        "@com_github_grailbio_base//unsafe:go_default_library",
        "@com_github_grailbio_hts//sam:go_default_library",
        "@io_v_x_lib//cmdline:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "checksum_test.go",
        "filter_test.go",
        "flagstat_test.go",
        "view_test.go",
    ],
    embed = [":go_default_library"],
    deps = [
        "@com_github_grailbio_hts//sam:go_default_library",
        "@com_github_grailbio_testutil//:go_default_library",
        "@com_github_stretchr_testify//assert:go_default_library",
        "@com_github_stretchr_testify//require:go_default_library",
        "@io_v_x_lib//gosh:go_default_library",
    ],
)
