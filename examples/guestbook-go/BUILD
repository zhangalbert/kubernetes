package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
)

go_binary(
    name = "guestbook-go",
    embed = [":go_default_library"],
    importpath = "k8s.io/kubernetes/examples/guestbook-go",
)

go_library(
    name = "go_default_library",
    srcs = ["main.go"],
    importpath = "k8s.io/kubernetes/examples/guestbook-go",
    deps = [
        "//vendor/github.com/codegangsta/negroni:go_default_library",
        "//vendor/github.com/gorilla/mux:go_default_library",
        "//vendor/github.com/xyproto/simpleredis:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)
