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

load("@bazel_skylib//:bzl_library.bzl", "bzl_library")
load("@rules_java//java:defs.bzl", "java_library")
load(":test.bzl", "all_tests")

licenses(["notice"])

LOCAL_TESTS = [
    "InfoTest.java",
    "MigrateCmdTest.java",
    "util/DiffUtilTest.java",
    "util/AutoPatchUtilTest.java",
    "util/ConsistencyFileTest.java",
    "util/ApplyDestinationPatchTest.java",
    "WorkflowTest.java",
]

all_tests(
    name = "info_test",
    shard_count = 3,
    tags = ["local"],
    tests = ["InfoTest.java"],
    deps = [
        "//java/com/google/copybara:base",
        "//java/com/google/copybara:copybara_lib",
        "//java/com/google/copybara/authoring",
        "//java/com/google/copybara/config:base",
        "//java/com/google/copybara/config:parser",
        "//java/com/google/copybara/exception",
        "//java/com/google/copybara/revision",
        "//java/com/google/copybara/testing",
        "//java/com/google/copybara/util",
        "//java/com/google/copybara/util/console",
        "//java/com/google/copybara/util/console/testing",
        "//third_party:mockito",
        "//third_party:truth",
    ],
)

all_tests(
    name = "migrate_cmd_test",
    shard_count = 2,
    tags = ["local"],
    tests = ["MigrateCmdTest.java"],
    deps = [
        "//java/com/google/copybara:copybara_lib",
        "//java/com/google/copybara/config:base",
        "//java/com/google/copybara/exception",
        "//java/com/google/copybara/git",
        "//java/com/google/copybara/git:core",
        "//java/com/google/copybara/revision",
        "//java/com/google/copybara/testing",
        "//java/com/google/copybara/testing/git",
        "//java/com/google/copybara/util",
        "//java/com/google/copybara/util/console",
        "//java/com/google/copybara/util/console/testing",
        "//third_party:truth",
    ],
)

all_tests(
    name = "diff_util_test",
    shard_count = 5,
    tags = ["local"],
    tests = ["util/DiffUtilTest.java"],
    deps = [
        "//java/com/google/copybara/git:environment",
        "//java/com/google/copybara/util",
        "//third_party:shell",
        "//third_party:truth",
    ],
)

all_tests(
    name = "auto_patch_util_test",
    shard_count = 2,
    tags = ["local"],
    tests = ["util/AutoPatchUtilTest.java"],
    deps = [
        "//java/com/google/copybara/util",
        "//third_party:truth",
    ],
)

java_library(
    name = "consistency_file_tests_lib",
    testonly = 1,
    srcs = ["util/ConsistencyFileTest.java"],
    visibility = ["//visibility:public"],
    deps = [
        "//java/com/google/copybara/exception",
        "//java/com/google/copybara/testing",
        "//java/com/google/copybara/util:consistency",
        "//third_party:guava",
        "//third_party:junit",
        "//third_party:truth",
    ],
)

all_tests(
    name = "consistency_file_tests",
    shard_count = 1,
    tags = ["local"],
    tests = [
        "util/ConsistencyFileTest.java",
    ],
    deps = [
        "//java/com/google/copybara/exception",
        "//java/com/google/copybara/testing",
        "//java/com/google/copybara/util:consistency",
        "//third_party:truth",
    ],
)

java_library(
    name = "workflow_test_lib",
    testonly = 1,
    srcs = ["WorkflowTest.java"],
    visibility = ["//visibility:public"],
    deps = [
        "//java/com/google/copybara:base",
        "//java/com/google/copybara:copybara_lib",
        "//java/com/google/copybara/authoring",
        "//java/com/google/copybara/config:base",
        "//java/com/google/copybara/effect",
        "//java/com/google/copybara/exception",
        "//java/com/google/copybara/git",
        "//java/com/google/copybara/git:core",
        "//java/com/google/copybara/hg",
        "//java/com/google/copybara/monitor",
        "//java/com/google/copybara/remotefile",
        "//java/com/google/copybara/revision",
        "//java/com/google/copybara/testing",
        "//java/com/google/copybara/testing/git",
        "//java/com/google/copybara/util",
        "//java/com/google/copybara/util:consistency",
        "//java/com/google/copybara/util/console",
        "//java/com/google/copybara/util/console/testing",
        "//third_party:guava",
        "//third_party:jimfs",
        "//third_party:jsr305",
        "//third_party:junit",
        "//third_party:mockito",
        "//third_party:starlark",
        "//third_party:truth",
    ],
)

all_tests(
    name = "workflow_test",
    shard_count = 5,
    tags = ["local"],
    tests = ["WorkflowTest.java"],
    deps = [
        "//java/com/google/copybara:base",
        "//java/com/google/copybara:copybara_lib",
        "//java/com/google/copybara/authoring",
        "//java/com/google/copybara/config:base",
        "//java/com/google/copybara/effect",
        "//java/com/google/copybara/exception",
        "//java/com/google/copybara/git:core",
        "//java/com/google/copybara/git:environment",
        "//java/com/google/copybara/hg",
        "//java/com/google/copybara/monitor",
        "//java/com/google/copybara/remotefile",
        "//java/com/google/copybara/revision",
        "//java/com/google/copybara/testing",
        "//java/com/google/copybara/testing/git",
        "//java/com/google/copybara/util",
        "//java/com/google/copybara/util:consistency",
        "//java/com/google/copybara/util/console",
        "//java/com/google/copybara/util/console/testing",
        "//third_party:jimfs",
        "//third_party:mockito",
        "//third_party:starlark",
        "//third_party:truth",
    ],
)

all_tests(
    name = "all_tests",
    data = [
        "//java/com/google/copybara:reference.md",
    ],
    env = {"REFERENCE_DIR": "$(rlocationpath //java/com/google/copybara:reference.md)"},
    tests = glob(
        ["**/*Test.java"],
        exclude = LOCAL_TESTS,
    ),
    deps = [
        "//java/com/google/copybara:base",
        "//java/com/google/copybara:copybara_lib",
        "//java/com/google/copybara:copybara_main",
        "//java/com/google/copybara:labels",
        "//java/com/google/copybara:starlark_date_time_module",
        "//java/com/google/copybara/authoring",
        "//java/com/google/copybara/checks",
        "//java/com/google/copybara/config:base",
        "//java/com/google/copybara/doc:annotations",
        "//java/com/google/copybara/effect",
        "//java/com/google/copybara/exception",
        "//java/com/google/copybara/monitor",
        "//java/com/google/copybara/revision",
        "//java/com/google/copybara/testing",
        "//java/com/google/copybara/transform",
        "//java/com/google/copybara/util",
        "//java/com/google/copybara/util:origin_util",
        "//java/com/google/copybara/util/console",
        "//java/com/google/copybara/util/console/testing",
        "//third_party:google_code_gson",
        "//third_party:guava_testlib",
        "//third_party:jcommander",
        "//third_party:jimfs",
        "//third_party:mockito",
        "//third_party:re2j",
        "//third_party:shell",
        "//third_party:starlark",
        "//third_party:testparameterinjector",
        "//third_party:truth",
    ],
)

bzl_library(
    name = "test_bzl",
    srcs = ["test.bzl"],
    # Used for extending the tests internally. Not a public API.
    visibility = ["//visibility:public"],
    deps = ["@rules_java//java:rules"],
)

java_library(
    name = "patchtests",
    testonly = True,
    srcs = [
        "util/AutoPatchUtilTest.java",
        "util/DiffUtilTest.java",
    ],
    # Used for extending the tests internally. Not a public API.
    visibility = ["//visibility:public"],
    deps = [
        "//java/com/google/copybara/git",
        "//java/com/google/copybara/util",
        "//third_party:guava",
        "//third_party:junit",
        "//third_party:shell",
        "//third_party:truth",
    ],
)

java_library(
    name = "apply_destination_patch_tests_lib",
    testonly = 1,
    srcs = ["util/ApplyDestinationPatchTest.java"],
    visibility = ["//visibility:public"],
    deps = [
        "//java/com/google/copybara/util",
        "//java/com/google/copybara/util/console",
        "//java/com/google/copybara/util/console/testing",
        "//third_party:guava",
        "//third_party:junit",
        "//third_party:truth",
    ],
)

all_tests(
    name = "apply_destination_patch_tests",
    tags = ["local"],
    tests = ["util/ApplyDestinationPatchTest.java"],
    deps = [
        "//java/com/google/copybara/util",
        "//java/com/google/copybara/util/console",
        "//java/com/google/copybara/util/console/testing",
        "//third_party:truth",
    ],
)
