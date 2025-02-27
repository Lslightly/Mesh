# Copyright 2020 The Mesh Authors. All rights reserved.
# Use of this source code is governed by the Apache License,
# Version 2.0, that can be found in the LICENSE file.

workspace(name = "org_libmesh")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Hedron's Compile Commands Extractor for Bazel
# https://github.com/hedronvision/bazel-compile-commands-extractor
http_archive(
    name = "hedron_compile_commands",

    # Replace the commit hash (6d29d97b4a40143104cce158b0da848db72cb769) in both places (below) with the latest (https://github.com/hedronvision/bazel-compile-commands-extractor/commits/main), rather than using the stale one here.
    # Even better, set up Renovate and let it do the work for you (see "Suggestion: Updates" in the README).
    url = "https://github.com/hedronvision/bazel-compile-commands-extractor/archive/6d29d97b4a40143104cce158b0da848db72cb769.tar.gz",
    strip_prefix = "bazel-compile-commands-extractor-6d29d97b4a40143104cce158b0da848db72cb769",
    # When you first run this tool, it'll recommend a sha256 hash to put here with a message like: "DEBUG: Rule 'hedron_compile_commands' indicated that a canonical reproducible form can be obtained by modifying arguments sha256 = ..."
)
load("@hedron_compile_commands//:workspace_setup.bzl", "hedron_compile_commands_setup")
hedron_compile_commands_setup()
load("@hedron_compile_commands//:workspace_setup_transitive.bzl", "hedron_compile_commands_setup_transitive")
hedron_compile_commands_setup_transitive()
load("@hedron_compile_commands//:workspace_setup_transitive_transitive.bzl", "hedron_compile_commands_setup_transitive_transitive")
hedron_compile_commands_setup_transitive_transitive()
load("@hedron_compile_commands//:workspace_setup_transitive_transitive_transitive.bzl", "hedron_compile_commands_setup_transitive_transitive_transitive")
hedron_compile_commands_setup_transitive_transitive_transitive()



load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

commit = {
    "rules_cc": "aa7ff810cf5ec99ca34f784743b33631b74c2d16",
    "googletest": "aa533abfd4232b01f9e57041d70114d5a77e6de0",
    "benchmark": "bc5651e54a7e178ca6b1e27e469a9be19cfa62c4", # 1.5.4
    "heap_layers": "f97c110c6a06982284e8927d17e52129736aa123",
}

http_archive(
    name = "rules_cc",
    sha256 = "21749f1be88e0965a1e70eed1a433d73c0ceaf485dfa50ff2d6e7c6944917673",
    strip_prefix = "rules_cc-{}".format(commit["rules_cc"]),
    urls = [
        "https://github.com/bazelbuild/rules_cc/archive/{}.zip".format(commit["rules_cc"]),
    ],
)

http_archive(
    name = "com_google_googletest",
    sha256 = "ab7d3be1f3781984102d7c12d7dc27ae2695a817c439f24db8ffc593840c1b17",
    strip_prefix = "googletest-{}".format(commit["googletest"]),
    urls = [
        "https://github.com/google/googletest/archive/{}.zip".format(commit["googletest"]),
    ],
)

http_archive(
    name = "com_google_benchmark",
    sha256 = "",
    strip_prefix = "benchmark-{}".format(commit["benchmark"]),
    urls = [
        "https://github.com/google/benchmark/archive/{}.zip".format(commit["benchmark"]),
    ],
)

http_archive(
    name = "org_heaplayers",
    sha256 = "ee2c351be580f2242bfccef6cc092166d009e773bc42154aa9af0fb1f1bd4fcf",
    strip_prefix = "Heap-Layers-{}".format(commit["heap_layers"]),
    urls = [
        "https://github.com/emeryberger/Heap-Layers/archive/{}.zip".format(commit["heap_layers"]),
    ],
)
