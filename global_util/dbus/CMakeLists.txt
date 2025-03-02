# SPDX-FileCopyrightText: 2023 UnionTech Software Technology Co., Ltd.
#
# SPDX-License-Identifier: GPL-3.0-or-later

set (SESSION_UI_DBUS_INTERFACE_SRCS
    com_deepin_chromeextension_tabslimit.cpp
    com_deepin_chromeextension_tabslimit.h
    org_deepin_dde_accounts1.cpp
    org_deepin_dde_accounts1.h
    org_deepin_dde_accounts1_user.cpp
    org_deepin_dde_accounts1_user.h
    org_deepin_dde_appearance1.cpp
    org_deepin_dde_appearance1.h
    org_deepin_dde_audio1.cpp
    org_deepin_dde_audio1.h
    org_deepin_dde_audio1_sink.cpp
    org_deepin_dde_audio1_sink.h
    org_deepin_dde_bluetooth1.cpp
    org_deepin_dde_bluetooth1.h
    org_deepin_dde_daemon_dock1.cpp
    org_deepin_dde_daemon_dock1.h
    org_deepin_dde_daemon_launcherd1.cpp
    org_deepin_dde_daemon_launcherd1.h
    org_deepin_dde_display1.cpp
    org_deepin_dde_display1.h
    org_deepin_dde_display1_monitor.cpp
    org_deepin_dde_display1_monitor.h
    org_deepin_dde_gesture1.cpp
    org_deepin_dde_gesture1.h
    org_deepin_dde_imageblur1.cpp
    org_deepin_dde_imageblur1.h
    org_deepin_dde_inputdevice1_keyboard.cpp
    org_deepin_dde_inputdevice1_keyboard.h
    org_deepin_dde_notification1.cpp
    org_deepin_dde_notification1.h
    org_deepin_dde_sessionmanager1.cpp
    org_deepin_dde_sessionmanager1.h
    org_deepin_dde_soundeffect1.cpp
    org_deepin_dde_soundeffect1.h
    org_deepin_dde_startmanager1.cpp
    org_deepin_dde_startmanager1.h

    types/appscgroupinfo.h
    types/appscgroupinfolist.cpp
    types/appscgroupinfolist.h
    types/audioport.cpp
    types/audioport.h
    types/audioportlist.cpp
    types/audioportlist.h
    types/brightnessmap.cpp
    types/brightnessmap.h
    types/dockrect.cpp
    types/dockrect.h
    types/keyboardlayoutlist.cpp
    types/keyboardlayoutlist.h
    types/launcheriteminfo.cpp
    types/launcheriteminfo.h
    types/launcheriteminfolist.cpp
    types/launcheriteminfolist.h
    types/qrect.h
    types/qvariantmap.cpp
    types/qvariantmap.h
    types/reflectlist.cpp
    types/reflectlist.h
    types/resolution.cpp
    types/resolution.h
    types/resolutionlist.cpp
    types/resolutionlist.h
    types/rotationlist.cpp
    types/rotationlist.h
    types/screenrect.cpp
    types/screenrect.h
    types/touchscreeninfolist.cpp
    types/touchscreeninfolist.h
    types/touchscreeninfolist_v2.cpp
    types/touchscreeninfolist_v2.h
    types/touchscreenmap.cpp
    types/touchscreenmap.h
)

add_library(session-ui-dbus-shared OBJECT
    ${SESSION_UI_DBUS_INTERFACE_SRCS}
)

target_include_directories(session-ui-dbus-shared
PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}
)

target_link_libraries(session-ui-dbus-shared
PRIVATE
    Qt5::DBus
    Dtk::Core
)
