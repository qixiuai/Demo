package(
    default_visibility = ["//visibility:public"],
)

licenses(["notice"])

cc_library(
    name = "lib3",
    hdrs = ["lib3.h"],
    deps = ["//psg/event:lib2", "//boost:boost"],
)

cc_binary(
    name = "demo",
    srcs = ["demo.cc"],
    deps = [":lib3"],
)
