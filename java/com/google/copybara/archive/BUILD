# Copyright 2023 Google LLC
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

java_library(
    name = "archive",
    srcs = glob(["**/*.java"]),
    deps = [
        "//java/com/google/copybara:base",
        "//java/com/google/copybara/archive/util",
        "//java/com/google/copybara/config:base",
        "//java/com/google/copybara/doc:annotations",  # unuseddeps: keep
        "//java/com/google/copybara/exception",
        "//java/com/google/copybara/remotefile/extractutil",
        "//java/com/google/copybara/util",
        "//third_party:guava",
        "//third_party:starlark",
    ],
)
