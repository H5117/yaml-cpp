project('yaml-cpp', 'cpp',
        version: '0.7.1',
        license: 'MIT',
        default_options: ['cpp_std=c++14'],
        meson_version:'>= 1.0.0'
       )

modpkgconfig = import('pkgconfig')

libyamlcpp = library('yaml-cpp',
    version: meson.project_version(),
    include_directories: 'include',
    sources: files(
        'src/binary.cpp',
        'src/convert.cpp',
        'src/depthguard.cpp',
        'src/directives.cpp',
        'src/emit.cpp',
        'src/emitfromevents.cpp',
        'src/emitter.cpp',
        'src/emitterstate.cpp',
        'src/emitterutils.cpp',
        'src/exceptions.cpp',
        'src/exp.cpp',
        'src/memory.cpp',
        'src/node.cpp',
        'src/node_data.cpp',
        'src/nodebuilder.cpp',
        'src/nodeevents.cpp',
        'src/null.cpp',
        'src/ostream_wrapper.cpp',
        'src/parse.cpp',
        'src/parser.cpp',
        'src/regex_yaml.cpp',
        'src/scanner.cpp',
        'src/scanscalar.cpp',
        'src/scantag.cpp',
        'src/scantoken.cpp',
        'src/simplekey.cpp',
        'src/singledocparser.cpp',
        'src/stream.cpp',
        'src/tag.cpp'
    ),
    install: true
)

depyamlcpp = declare_dependency(
    include_directories: 'include',
    link_with: libyamlcpp
)

install_subdir('include' / 'yaml-cpp',
    install_dir: get_option('includedir')
)

modpkgconfig.generate(
    libyamlcpp,
    name: 'yaml-cpp',
    version: meson.project_version(),
    description: 'A YAML parser and emitter in C++',
    url: 'https://github.com/jbeder/yaml-cpp',
    filebase: 'yaml-cpp'
)

if get_option('tests')
    subdir('test')
endif

