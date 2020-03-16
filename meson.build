project(
	'pw-video-src',
	'c',
	version: '0.0.0',
	license: 'MIT',
	meson_version: '>=0.46.0',
	default_options: [
		'c_std=c11',
		'warning_level=2',
		'werror=true',
	],
)

cc = meson.get_compiler('c')

add_project_arguments(cc.get_supported_arguments([
	'-Wno-missing-braces',
	'-Wno-missing-field-initializers',
	'-Wno-unused-parameter',
]), language: 'c')

pipewire = dependency('libpipewire-0.3', version: '>= 0.2.9')

executable(
	'video-src',
	files([
		'video-src.c',
	]),
	dependencies: [
		pipewire,
	],
)
