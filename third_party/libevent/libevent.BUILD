load("@rules_foreign_cc//foreign_cc:defs.bzl", "cmake")

licenses(["notice"])

filegroup(
    name = "all",
    srcs = glob(["**"]),
)

cmake(
    name = "libevent",
    cache_entries = {
        "EVENT__DISABLE_OPENSSL": "on",
        "EVENT__DISABLE_MBEDTLS": "on",
        "EVENT__DISABLE_REGRESS": "on",
        "EVENT__DISABLE_TESTS": "on",
        "EVENT__LIBRARY_TYPE": "SHARED",
        "_GNU_SOURCE": "on",
    },
    lib_source = ":all",
    out_shared_libs = ["libevent-2.1.so.7"],
    visibility = ["//visibility:public"],
)
