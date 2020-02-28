load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["distance.go"],
    importpath = "github.com/josh-newman/bio/util",
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_test",
    srcs = ["distance_test.go"],
    embed = [":go_default_library"],
    deps = ["@com_github_antzucaro_matchr//:go_default_library"],
)
