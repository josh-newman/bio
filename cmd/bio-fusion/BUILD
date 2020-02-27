load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["main.go"],
    importpath = "github.com/josh-newman/bio/cmd/bio-fusion",
    visibility = ["//visibility:private"],
)

go_binary(
    name = "bio-fusion",
    embed = [":go_default_library"],
    visibility = ["//visibility:public"],
)
