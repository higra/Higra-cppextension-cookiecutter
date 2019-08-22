set(TEST_FILES
        test_extension.py)

foreach (FILE ${TEST_FILES})
    configure_file(${FILE} ${CMAKE_CURRENT_BINARY_DIR}/${FILE} COPYONLY)
endforeach ()
        
add_custom_target(all_tests ALL
        DEPENDS {{ cookiecutter.python_package_name }}
        )

if (DO_AUTO_TEST)
    add_custom_command(TARGET all_tests
        COMMENT "Run tests"
        POST_BUILD COMMAND ${PYTHON_EXECUTABLE} -c \"import sys\;sys.path.insert(0, '${CMAKE_LIBRARY_OUTPUT_DIRECTORY}')\;import unittest\;result=unittest.TextTestRunner().run(unittest.defaultTestLoader.discover('${CMAKE_CURRENT_BINARY_DIR}'))\;exit(0 if result.wasSuccessful() else 1)\" 
            WORKING_DIRECTORY ${CMAKE_BINARY_DIR}
            )
endif ()
