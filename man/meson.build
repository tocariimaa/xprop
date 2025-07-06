sed = find_program('sed')
xprop_version = 'xprop @0@'.format(meson.project_version())

custom_target(
  'xprop.man',
  input: 'xprop.man',
  output: 'xprop.1',
  capture: true,
  install: true,
  install_dir: '.',
  command: [
    sed,
    '-e', f's/__vendorversion__/"@xprop_version@" "X Version 11"/g',
    '@INPUT@'
  ],
)
