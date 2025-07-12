workspace(name = "zach_sandbox")

load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Load external lib macros
load(
    "//repositories:repositories.bzl",
    "load_cloud_archive",
)

bazel_dep(name = "rules_cc", version = "0.0.17")

##################### S3 Rules ######################

load_cloud_archive()

##################### End S3 Rules ##################

# Generate compile_commands.json
load("//repositories/hedron_compile_commands:hedron_compile_commands.bzl", "load_hedron_compile_commands")

load_hedron_compile_commands()

load("@hedron_compile_commands//:workspace_setup.bzl", "hedron_compile_commands_setup")

hedron_compile_commands_setup()

# load_pcl()

# load("@rules_pcl//bzl:repositories.bzl", "pcl_repositories")

# pcl_repositories()

# load("@rules_pcl//bzl:init_deps.bzl", "pcl_init_deps")

# pcl_init_deps()

# load("//repositories/tl_expected:tl_expected.bzl", "load_tl_expected")

# load_tl_expected()

# load("//repositories/taywee_args:taywee_args.bzl", "load_taywee_args")

# load_taywee_args()

#################### Common Tools ###################

git_repository(
    name = "gtest",
    remote = "https://github.com/google/googletest",
    branch = "v1.13.x",
)

#################### End Common Tools ###############
