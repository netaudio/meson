project('subproject targets', 'c')

# Idea behind this test is to create targets with identical name
# but different output files. We can do this by choosing different
# name_prefix of libraries. Target id does not depend on name_prefix.

main_foo = static_library('foo', 'foo.c', name_prefix : 'main')
subproj_foo = subproject('subproj').get_variable('foo')

exe = executable('prog', 'main.c', link_with : [main_foo, subproj_foo])
test('main test', exe)
