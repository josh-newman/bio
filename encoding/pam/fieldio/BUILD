load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "bytebuffer.go",
        "reader.go",
        "unsafearena.go",
        "unsafeint32.go",
        "writer.go",
    ],
    importpath = "github.com/josh-newman/bio/encoding/pam/fieldio",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_grailbio_base//errors:go_default_library",
        "@com_github_grailbio_base//file:go_default_library",
        "@com_github_grailbio_base//log:go_default_library",
        "@com_github_grailbio_base//recordio:go_default_library",
        "@com_github_grailbio_base//recordio/recordioiov:go_default_library",
        "@com_github_grailbio_base//syncqueue:go_default_library",
        "@com_github_grailbio_base//traverse:go_default_library",
        "@com_github_grailbio_base//unsafe:go_default_library",
        "@com_github_grailbio_base//vcontext:go_default_library",
        "@com_github_grailbio_hts//sam:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["bytebuffer_test.go"],
    embed = [":go_default_library"],
    deps = ["@com_github_grailbio_testutil//expect:go_default_library"],
)
