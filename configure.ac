AC_INIT(
    [ceti-2-theme],
    [20150425],
    [https://github.com/horst3180/Ceti-2-theme/issues],
    [ceti-2-theme],
    [https://github.com/horst3180/Ceti-2-theme],
    []
)

AC_CONFIG_AUX_DIR([build-aux])
AC_CONFIG_MACRO_DIR([m4])
AM_INIT_AUTOMAKE([foreign])
AC_PROG_MKDIR_P

CETI_ENABLE([GNOME_SHELL], [gnome-shell], [GNOME Shell],  [disable])
CETI_ENABLE([GTK2],        [gtk2],        [GTK2],         [disable])
CETI_ENABLE([GTK3],        [gtk3],        [GTK3],         [disable])
CETI_ENABLE([METACITY],    [metacity],    [Metacity],     [disable])
CETI_ENABLE([UNITY],       [unity],       [Unity],        [disable])
CETI_ENABLE([XFWM],        [xfwm],        [XFWM],         [disable])

CETI_GNOME

AC_CONFIG_FILES([
    common/Makefile
    extra/Makefile
    Makefile
])

AC_OUTPUT
