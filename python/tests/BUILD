cc_test(
    name = "cc_deps_link_test",
    size = "small",
    srcs = [
        "cc_deps_link_test.cc",
    ],
    copts = [
        "-std=c++17",
        # Compiling against upstream Tensorflow headers requires -std=c++17 due
        # (at least) to Tensorflow's use of the type trait
        # std::is_arithmetic_v, which was introduced in C++17.
        #
        # TODO(b/271210933): Harmonize this with a global solution
        # throughout the repository. Presumably this same issue will be
        # encountered by other code compiling against upstream Tensorflow,
        # such as custom operator implementations.
    ],
    deps = [
        "@tensorflow_cc_deps//:cc_library",
    ],
)
