workspace(name = "bazel_gazelle")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_go",
    sha256 = "ac03931e56c3b229c145f1a8b2a2ad3e8d8f1af57e43ef28a26123362a1e3c7e",
    urls = [
        "https://mirror.bazel.build/github.com/bazelbuild/rules_go/releases/download/v0.24.4/rules_go-v0.24.4.tar.gz",
        "https://github.com/bazelbuild/rules_go/releases/download/v0.24.4/rules_go-v0.24.4.tar.gz",
    ],
)

load("@io_bazel_rules_go//go:deps.bzl", "go_register_toolchains", "go_rules_dependencies")

go_rules_dependencies()

go_register_toolchains()

go_register_toolchains(nogo = "@bazel_gazelle//:nogo")

load("//:deps.bzl", "gazelle_dependencies")

gazelle_dependencies()

# gazelle:repository go_repository name=org_golang_x_sync importpath=golang.org/x/sync
# gazelle:repository go_repository name=org_golang_x_sys importpath=golang.org/x/sys
# gazelle:repository go_repository name=org_golang_x_xerrors importpath=golang.org/x/xerrors
# gazelle:repository go_repository name=com_github_bazelbuild_buildtools importpath=github.com/bazelbuild/buildtools build_naming_convention=go_default_library
# gazelle:repository go_repository name=com_github_fsnotify_fsnotify importpath=github.com/fsnotify/fsnotify
# gazelle:repository go_repository name=com_github_pelletier_go_toml importpath=github.com/pelletier/go-toml
# gazelle:repository go_repository name=com_github_pmezard_go_difflib importpath=github.com/pmezard/go-difflib
# gazelle:repository go_repository name=com_github_bmatcuk_doublestar importpath=github.com/bmatcuk/doublestar
# gazelle:repository go_repository name=com_github_google_go_cmp importpath=github.com/google/go-cmp
