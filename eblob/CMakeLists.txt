LOCATE_LIBRARY(LIBEBLOB "eblob.hpp" "eblob_cpp" "eblob")

ADD_LIBRARY(eblob MODULE
    eblob)

TARGET_LINK_LIBRARIES(eblob
    cocaine-common
    eblob_cpp)

SET_TARGET_PROPERTIES(eblob PROPERTIES
    PREFIX ""
    SUFFIX "${COCAINE_PLUGIN_SUFFIX}"
)

INSTALL(TARGETS eblob
    LIBRARY DESTINATION lib/cocaine
    COMPONENT runtime)
