load("@bazel_gazelle//:def.bzl", "gazelle")

# gazelle:prefix github.com/grailbio/bio

gazelle(
    name = "gazelle",
    command = "fix",
    extra_args = [
        "-build_file_name=BUILD",
        "-build_tags=bazel",
    ],
)
