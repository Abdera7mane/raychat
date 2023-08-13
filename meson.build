project('raychat', 'c',
  version : '0.1',
  default_options : [
    'warning_level=3',
    'b_coverage=true',
    'b_pie=true',
  ])

cc = meson.get_compiler('c')
cmake = import('cmake')

raylib_options = cmake.subproject_options()
raylib_options.set_install(false)
raylib_options.add_cmake_defines({
  'BUILD_EXAMPLES': 'OFF',
  'PLATFORM': 'Desktop',
})

add_global_arguments('-DGRAPHICS_API_OPENGL_21', language: 'c')

raylib = cmake.subproject('raylib', options: raylib_options)

dependencies = [
  cc.find_library('m', required : true),
  cc.find_library('dl', required : true),
  raylib.dependency('raylib'),
  raylib.dependency('glfw'),
  dependency('raygui'),
]

include = [
 'src'
]

sources = [
  'src/main.c',
]

program = executable('raychat',
  sources,
  include_directories : include,
  dependencies : dependencies,
  install : true)

