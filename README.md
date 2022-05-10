```
$ bazel build //b:b
ERROR: /Users/john/figma/rules_rust_duplicate_module_mapping/b/BUILD.bazel:4:11: in @build_bazel_rules_nodejs//internal/common:module_mappings.bzl%module_mappings_runtime_aspect aspect on ts_project rule //b:tsc:
Traceback (most recent call last):
	File "/private/var/tmp/_bazel_johnfirebaugh/2eba95c510d0d05d3c27e1afb2df478f/external/build_bazel_rules_nodejs/internal/common/module_mappings.bzl", line 106, column 36, in _module_mappings_runtime_aspect_impl
		mappings = _get_module_mappings(target, ctx)
	File "/private/var/tmp/_bazel_johnfirebaugh/2eba95c510d0d05d3c27e1afb2df478f/external/build_bazel_rules_nodejs/internal/common/module_mappings.bzl", line 67, column 21, in _get_module_mappings
		fail(("duplicate module mapping at %s: %s maps to both %s and %s" %
Error in fail: duplicate module mapping at //b:tsc: @types/node maps to both npm_a/node_modules/@types/node and npm_b/node_modules/@types/node deps
ERROR: Analysis of target '//b:b' failed; build aborted:
INFO: Elapsed time: 7.890s
INFO: 0 processes.
FAILED: Build did NOT complete successfully (53 packages loaded, 452 targets configured)
```
