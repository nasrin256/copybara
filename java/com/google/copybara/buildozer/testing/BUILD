# Copyright 2016 Google Inc.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

load("@rules_java//java:defs.bzl", "java_library")

package(default_visibility = ["//visibility:public"])

licenses(["notice"])

genrule(
    name = "normalised_buildozer",
    testonly = 1,
    srcs = ["@buildifier_prebuilt//:buildozer"],
    outs = ["buildozer"],
    cmd = "cp $(SRCS) $@",
)

genrule(
    name = "normalised_buildifier",
    testonly = 1,
    srcs = ["@buildifier_prebuilt//:buildifier"],
    outs = ["buildifier"],
    cmd = "cp $(SRCS) $@",
)

java_library(
    name = "testing",
    testonly = 1,
    srcs = glob(["*.java"]),
    data = [
        ":normalised_buildifier",
        ":normalised_buildozer",
    ],
    deps = [
        "//java/com/google/copybara/testing",
    ],
)
