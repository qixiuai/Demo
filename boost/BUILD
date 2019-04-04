
package(
    default_visibility = ["//visibility:public"],
)

licenses(["notice"])

cc_library(
    name = "boost",
    hdrs = glob(["include/**/*.hpp"]),
    includes = ["include"],
    deps = select({
        "@bazel_tools//src/conditions:windows" :
        [
            ":boost_system_win",
            ":boost_date_time_win",
            ":boost_regex_win",
        ],
        "//conditions:default" :
        [
            ":boost_system_linux",
#            ":boost_date_time_linux",
#            ":boost_atomic_linux",
#            ":boost_chrono_linux",
            ":boost_filesystem_linux",
#            ":boost_random_linux",
#            ":boost_regex_linux",
#            ":boost_serialization_linux",
#            ":boost_thread_linux",
        ],
    }),
)

cc_import(
    name = "boost_system_linux",
    shared_library = "lib/libboost_system.so",
)

cc_import(
    name = "boost_system_win",
    interface_library = "lib/boost_system-vc140-mt.lib",
    shared_library = "lib/boost_system-vc141-mt-x64-1_69.dll",
)

cc_import(
    name = "boost_date_time_linux",
    shared_library = "lib/libboost_date_time.so",
)

cc_import(
    name = "boost_date_time_win",
    interface_library = "lib/boost_date_time-vc140-mt.lib",
    shared_library = "lib/boost_date_time-vc141-mt-x64-1_69.dll",
)

cc_import(
    name = "boost_regex_linux",
    shared_library = "lib/libboost_regex.so",
)

cc_import(
    name = "boost_regex_win",
    interface_library = "lib/boost_regex-vc140-mt.lib",
    shared_library = "lib/boost_regex-vc141-mt-x64-1_69.dll",
)

cc_import(
    name = "boost_chrono_linux",
    shared_library = "lib/libboost_chrono.so",
)

cc_import(
    name = "boost_filesystem_linux",
    shared_library = "lib/libboost_filesystem.so",
)

cc_import(
    name = "boost_random_linux",
    shared_library = "lib/libboost_random.so",
)

cc_import(
    name = "boost_thread_linux",
    shared_library = "lib/libboost_thread.so",
)

cc_import(
    name = "boost_atomic_linux",
    shared_library = "lib/libboost_atomic.so",
)

cc_import(
    name = "boost_serialization_linux",
    shared_library = "lib/libboost_serialization.so",
)
