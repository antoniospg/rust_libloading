project(
  'libloading',
  'rust',
  version : '0.8',
  license :'ISC',
  default_options : ['rust_std=2018'],
)

rc = meson.get_compiler('rust')

rust_args = [
]

cfg_if = subproject('cfg-if').get_variable('lib')

lib = static_library(
  'libloading',
  'src/lib.rs',
  rust_args : rust_args,
  link_with : [cfg_if],
  rust_crate_type : 'rlib'
)

dep_libloading = declare_dependency(
  link_with : [lib, cfg_if],
)
