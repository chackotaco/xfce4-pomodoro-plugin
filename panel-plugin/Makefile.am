AM_CPPFLAGS = \
	-I$(top_srcdir) \
	-DG_LOG_DOMAIN=\"xfce4-pomodoro-plugin\" \
	-DPACKAGE_LOCALE_DIR=\"$(localedir)\" \
	$(PLATFORM_CPPFLAGS)

#
# Sample plugin
#
plugin_LTLIBRARIES = \
	libxfcepomodoro.la

plugindir = \
	$(libdir)/xfce4/panel/plugins

libxfcepomodoro_la_SOURCES = \
	xfcepomodoro.c \
	xfcepomodoro.h \
	xfcepomodoro-dialogs.c \
	xfcepomodoro-dialogs.h \
	xfcepomodoro-config.c \
	xfcepomodoro-config.h \
	xfcepomodoro-timer.c \
	xfcepomodoro-timer.h

libxfcepomodoro_la_CFLAGS = \
	$(LIBXFCE4UTIL_CFLAGS) \
	$(LIBXFCE4UI_CFLAGS) \
	$(LIBXFCE4PANEL_CFLAGS) \
	$(PLATFORM_CFLAGS)

libxfcepomodoro_la_LDFLAGS = \
       -avoid-version \
       -module \
       -no-undefined \
       -export-symbols-regex '^xfce_panel_module_(preinit|init|construct)' \
       $(PLATFORM_LDFLAGS)

libxfcepomodoro_la_LIBADD = \
	$(LIBXFCE4UTIL_LIBS) \
	$(LIBXFCE4UI_LIBS) \
	$(LIBXFCE4PANEL_LIBS)

#
# Desktop file
#
desktopdir =								\
	$(datadir)/xfce4/panel/plugins

desktop_DATA =								\
	xfce4-pomodoro-plugin.desktop

@INTLTOOL_DESKTOP_RULE@

EXTRA_DIST =								\
	xfce4-pomodoro-plugin.desktop.in

CLEANFILES =								\
	$(desktop_DATA)

# vi:set ts=8 sw=8 noet ai nocindent syntax=automake:
