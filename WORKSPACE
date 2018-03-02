skylib_version = "f9b0ff1dd3d119d19b9cacbbc425a9e61759f1f5" # update this as needed
http_archive(
    name = "bazel_skylib",
    url = "https://github.com/bazelbuild/bazel-skylib/archive/%s.zip"%skylib_version,
    type = "zip",
    strip_prefix= "bazel-skylib-%s" % skylib_version
)

http_archive(
    name = "io_bazel_rules_go",
    url = "https://github.com/bazelbuild/rules_go/releases/download/0.10.0/rules_go-0.10.0.tar.gz",
    sha256 = "53c8222c6eab05dd49c40184c361493705d4234e60c42c4cd13ab4898da4c6be",
)
load("@io_bazel_rules_go//go:def.bzl", "go_rules_dependencies", "go_register_toolchains")
go_rules_dependencies()
go_register_toolchains()

rules_webtesting_version = "0b24d055fc51a61d5784952419916de722741d71" # update this as needed
http_archive(
    name = "io_bazel_rules_webtesting",
    url = "https://github.com/bazelbuild/rules_webtesting/archive/%s.zip"%rules_webtesting_version,
    type = "zip",
    strip_prefix= "rules_webtesting-%s" % rules_webtesting_version
)

load(
    "@io_bazel_rules_webtesting//web:repositories.bzl",
    "browser_repositories",
    "web_test_repositories"
)
web_test_repositories()

browser_repositories(
    chromium = True,
    firefox = True,
)
