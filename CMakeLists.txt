if (ESP_PLATFORM)
    set(COMPONENT_ADD_INCLUDEDIRS csrc)
    set(COMPONENT_SRCDIRS "csrc")
    set(COMPONENT_NAME "u8g2")

    register_component()
else ()
    #todo
endif ()

# must be added after idf register component
target_compile_options(${COMPONENT_LIB} PRIVATE -Wno-unused-const-variable)
