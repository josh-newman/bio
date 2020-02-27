load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "coord.go",
        "coord.pb.go",
        "pam.pb.go",
        "sort.pb.go",
    ],
    importpath = "github.com/josh-newman/bio/biopb",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_gogo_protobuf//gogoproto:go_default_library",
        "@com_github_gogo_protobuf//proto:go_default_library",
    ],
)
