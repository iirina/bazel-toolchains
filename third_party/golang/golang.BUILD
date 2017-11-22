# Copyright 2017 The Bazel Authors. All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#    http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

# This BUILD file is used for installing golang into /usr/local/go/
# of debian8-clang-fully-loaded container. It uses the official golang
# release tarball downloaded by new_http_archive rule in WORKSPACE file:
# https://storage.googleapis.com/golang/go1.9.1.linux-amd64.tar.gz

licenses(["notice"])  # Apache 2.0

package(default_visibility = ["//visibility:public"])

load("@bazel_tools//tools/build_defs/pkg:pkg.bzl", "pkg_tar")

pkg_tar(
    name = "tar",
    srcs = glob(["**/*"]),
    package_dir = "/usr/local/go/",
    strip_prefix = ".",
)
