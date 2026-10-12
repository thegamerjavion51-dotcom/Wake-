project('wake', 'c', default_options: ['c_std=gnu11', 'warning_level=1'])

wlroots   = dependency('wlroots-0.20')
scenefx   = dependency('scenefx-0.5')
cairo     = dependency('cairo')
cairo     = dependency('cairo')
wl_server = dependency('wayland-server')
xkb       = dependency('xkbcommon')
protos    = dependency('wayland-protocols')
scanner   = find_program('wayland-scanner')

xdg_xml = protos.get_variable('pkgdatadir') / 'stable/xdg-shell/xdg-shell.xml'
xdg_h = custom_target('xdg-shell-protocol.h',
  input: xdg_xml, output: 'xdg-shell-protocol.h',
  command: [scanner, 'server-header', '@INPUT@', '@OUTPUT@'])

executable('wake', ['wake.c', xdg_h],
  dependencies: [scenefx, wlroots, cairo, cairo, wl_server, xkb],
  c_args: ['-DWLR_USE_UNSTABLE'],
  install: true)
