sources = files(
    'ValaGist.vala',
    'Errors.vala',
    'Gist.vala',
    'GistFile.vala',
    'MyProfile.vala',
    'OtherProfile.vala',
    'Profile.vala'
)

valagist_static_lib = static_library('vala-gist', [sources], dependencies: deps, vala_args: [])
valagist_dep = declare_dependency(include_directories: include_directories('.'), link_with: valagist_static_lib)

# old dynamic lib
# valagist_lib = library('valagist-' + api_version, valagist_sources,
#		  vala_header: 'valagist-' + api_version + '.h',
#		  vala_vapi: 'valagist-' + api_version + '.vapi',
#		  dependencies: [glib, gobject, gio, json_glib, libsoup],
#                  vala_args: ['--vapidir=' + meson.current_source_dir()],
#                  c_args: ['-g', '-O0', '-Wno-unused'],
#                  install: true,
#                  install_dir: [true, true, true])
#
# valagist = declare_dependency(include_directories: include_directories('.'),
#                              link_with: valagist_lib)
#
## install_headers(meson.current_build_dir() +'/valagist-' + api_version + '.h', subdir: 'valagist-' + api_version)
## install_data(meson.current_build_dir() + '/valagist-' + api_version + '.vapi', install_dir: 'share/vala/vapi')
#
# pkgconfig = import('pkgconfig')
# pkgconfig.generate(name: 'valagist-' + api_version,
#                   description: 'Gist client library for Vala',
#                   version: meson.project_version(),
#                   filebase: 'valagist-' + api_version,
#                   requires: 'glib-2.0 gobject-2.0 json-glib-1.0 libsoup-2.4',
#                   libraries: valagist_lib,
#                   subdirs: 'valagist-' + api_version)
