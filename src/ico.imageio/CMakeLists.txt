# Copyright 2008-present Contributors to the OpenImageIO project.
# SPDX-License-Identifier: BSD-3-Clause
# https://github.com/OpenImageIO/oiio/blob/master/LICENSE.md

if (PNG_FOUND)
    add_oiio_plugin (icoinput.cpp icooutput.cpp
                     INCLUDE_DIRS ${PNG_INCLUDE_DIRS} ${ZLIB_INCLUDE_DIRS}
                     LINK_LIBRARIES ${PNG_LIBRARIES} ${ZLIB_LIBRARIES})
else ()
    message (WARNING "libpng not found, so ICO support will not work")
endif ()

