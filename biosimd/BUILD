load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "biosimd_amd64.go",
        "biosimd_amd64.s",
        "biosimd_generic.go",
        "count_amd64.go",
        "count_generic.go",
        "doc.go",
        "fastq_amd64.go",
        "fastq_amd64.s",
        "fastq_generic.go",
        "revcomp_amd64.go",
        "revcomp_amd64.s",
        "revcomp_generic.go",
    ],
    importpath = "github.com/grailbio/bio/biosimd",
    visibility = ["//visibility:public"],
    deps = select({
        "@io_bazel_rules_go//go/platform:386": [
            "@com_github_grailbio_base//simd:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:amd64": [
            "@com_github_grailbio_base//simd:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:amd64p32": [
            "@com_github_grailbio_base//simd:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:arm": [
            "@com_github_grailbio_base//simd:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:arm64": [
            "@com_github_grailbio_base//simd:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:mips": [
            "@com_github_grailbio_base//simd:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:mips64": [
            "@com_github_grailbio_base//simd:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:mips64le": [
            "@com_github_grailbio_base//simd:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:mipsle": [
            "@com_github_grailbio_base//simd:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:ppc64": [
            "@com_github_grailbio_base//simd:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:ppc64le": [
            "@com_github_grailbio_base//simd:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:s390x": [
            "@com_github_grailbio_base//simd:go_default_library",
        ],
        "//conditions:default": [],
    }),
)

go_test(
    name = "go_default_test",
    srcs = [
        "biosimd_test.go",
        "count_test.go",
        "fastq_test.go",
        "multi_benchmark_test.go",
        "revcomp_test.go",
    ],
    embed = [":go_default_library"],
    deps = [
        "@com_github_grailbio_base//simd:go_default_library",
        "@com_github_grailbio_base//traverse:go_default_library",
        "@com_github_grailbio_testutil//assert:go_default_library",
    ],
)
