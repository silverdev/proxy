# Copyright 2016 Istio Authors. All Rights Reserved.
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
#
################################################################################
#

load(
    "@envoy//bazel:envoy_build_system.bzl",
    "envoy_cc_library",
)

envoy_cc_library(
    name = "filter_lib",
    srcs = [
        "config.cc",
        "config.h",
        "grpc_transport.cc",
        "grpc_transport.h",
        "http_filter.cc",
        "mixer_control.cc",
        "mixer_control.h",
        "stats.cc",
        "stats.h",
        "tcp_filter.cc",
        "utils.cc",
        "utils.h",
    ],
    repository = "@envoy",
    visibility = ["//visibility:public"],
    deps = [
        "//external:mixer_http_control_lib",
        "//external:mixer_tcp_control_lib",
        "//src/envoy/auth:http_filter_lib",
        "@envoy//source/exe:envoy_common_lib",
    ],
)
