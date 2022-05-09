project('LEE example', 'c', 'cpp',
    version: '1.0',
    meson_version: '>=0.62.0',
)

libexample = library('example', 'somefile.c',
    install: true,
)

libexample_dep = declare_dependency(
    link_with: libexample,
    include_directories: include_directories('.'),
)

meson.override_dependency('example', libexample_dep)

pkg = import('pkgconfig')
pkg.generate(libexample)
