# Copyright 2025 Google LLC
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

load("//javatests/com/google/copybara:test.bzl", "all_tests")

all_tests(
    name = "all_tests",
    env = {"LC_CTYPE": "en_US.UTF-8"},
    tags = ["local"],
    tests = [
        "GitLabOptionsTest.java",
        "GitLabUtilTest.java",
    ],
    deps = [
        "//java/com/google/copybara/credentials",
        "//java/com/google/copybara/git:creds",
        "//java/com/google/copybara/git/gitlab:git_lab_options",
        "//java/com/google/copybara/git/gitlab:git_lab_util",
        "//java/com/google/copybara/git/gitlab/api:gitlab_api",
        "//java/com/google/copybara/http/auth",
        "//java/com/google/copybara/testing",
        "//java/com/google/copybara/util/console/testing",
        "//third_party:google_http_client",
        "//third_party:junit",
        "//third_party:mockito",
        "//third_party:truth",
    ],
)
