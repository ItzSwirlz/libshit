project('libshit', 'c',
  version : '0.1',
  default_options : ['warning_level=3'])

shlib = shared_library('shit', 'libshit.h',
  install : true,
  gnu_symbol_visibility : 'hidden',
)

# Make this library usable as a Meson subproject.
libshit_dep = declare_dependency(
  include_directories: include_directories('.'),
  link_with : shlib)

# Make this library usable from the system's
# package manager.
install_headers('libshit.h', subdir : 'libshit')

pkg_mod = import('pkgconfig')
pkg_mod.generate(
  name : 'libshit',
  filebase : 'libshit',
  description : 'Library for shit variables',
  subdirs : 'libshit',
  libraries : shlib,
  version : '0.1',
)
