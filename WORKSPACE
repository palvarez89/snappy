load("@bazel_tools//tools/build_defs/repo:git.bzl",
     "git_repository", "new_git_repository")

new_git_repository(
    name = "gtest",
    remote = "https://github.com/google/googletest.git",
    tag = "release-1.8.1",
    build_file = "gtest.BUILD",
    strip_prefix = "googletest",
)
