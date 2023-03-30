test('all',
    executable('yaml-cpp-tests',
        include_directories: '../src',
        sources: files(
            'integration/emitter_test.cpp',
            'integration/encoding_test.cpp',
            'integration/error_messages_test.cpp',
            'integration/gen_emitter_test.cpp',
            'integration/handler_spec_test.cpp',
            'integration/handler_test.cpp',
            'integration/load_node_test.cpp',
            'integration/node_spec_test.cpp',
            'node/node_test.cpp',
            'binary_test.cpp',
            'main.cpp',
            'ostream_wrapper_test.cpp',
            'parser_test.cpp',
            'regex_test.cpp'
        ), dependencies: [
            depyamlcpp,
            dependency('threads'),
            dependency('gmock')
        ]
    )
)
