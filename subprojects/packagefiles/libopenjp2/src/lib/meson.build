# source code for openjpeg project:
# Part 1 & 2:
subdir('openjp2')

# optionals components:
if get_option('build_jpip')
  subdir('openjpip')
endif

pkgconfig = import('pkgconfig')
pkgconfig.generate(
  openjp2_lib,
  name: 'libopenjp2',
  description: 'JPEG2000 library (Part 1 and 2)',
  version: meson.project_version(),
  libraries: openjp2_lib,
)
if get_option('build_jpip')
  pkgconfig.generate(
    openjpip_lib,
    name: 'libopenjpip',
    description: 'JPEG2000 Interactivity tools, APIs and protocols (Part 9)',
    version: meson.project_version(),
    libraries: openjpip_lib,
  )
endif
