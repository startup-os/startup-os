# THIS FILE IS AUTO-GENERATED

package(default_visibility = ["//visibility:public"])

load("//tools/checkstyle:checkstyle.bzl", "checkstyle_test")

proto_library(
    name = "data_proto",
    srcs = ["data.proto"],
)

java_proto_library(
    name = "data_java_proto",
    deps = [":data_proto"],
)

java_binary(
    name = "proto_vs_json_tool",
    srcs = ["ProtoVsJsonTool.java"],
    main_class = "com.google.startupos.examples.proto_vs_json.ProtoVsJsonTool",
    deps = [
        ":data_java_proto",
        "//common",
        "//common:dagger_with_annotation_processor",
        "//common/flags",
        "//third_party/maven/com/google/flogger:flogger_system_backend",
        "//third_party/maven/com/google/protobuf:protobuf_java_util",
        "//third_party/maven/javax/inject:javax_inject",
    ],
)

checkstyle_test(
    name = "proto_vs_json_tool-checkstyle",
    target = ":proto_vs_json_tool",
)
