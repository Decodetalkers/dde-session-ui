# SPDX-FileCopyrightText: 2023 UnionTech Software Technology Co., Ltd.
#
# SPDX-License-Identifier: GPL-3.0-or-later

set(OSD_Name dde-osd)

add_executable(${OSD_Name}
    main.cpp
)
target_include_directories(dde-osd-shared
PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}
)

target_link_libraries(${OSD_Name} PRIVATE
    dde-osd-shared
    session-ui-dbus-shared
    ${Test_Libraries}
)

## bin
install(TARGETS ${OSD_Name} DESTINATION lib/deepin-daemon)

## service
file(GLOB OSD_SERVICE_FILES "files/*.service")
install(FILES ${OSD_SERVICE_FILES} DESTINATION share/dbus-1/services)
