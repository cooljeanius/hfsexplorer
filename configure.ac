dnl#                                               -*- Autoconf -*-
dnl# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([hfsexplorer],[0_21],[/dev/null])
AC_CONFIG_AUX_DIR([build-aux])
AC_CONFIG_SRCDIR([src.win32/launcher/launcher.cpp])
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_MACRO_DIR([m4])
AC_CANONICAL_TARGET
AM_INIT_AUTOMAKE([foreign 1.11 no-installinfo dist-zip -Wall])
AM_MAINTAINER_MODE

AC_OBJEXT
AC_EXEEXT

# Checks for programs.
AM_PROG_AR
AC_PROG_CC
AC_PROG_CPP
AC_PROG_CXX
AM_PROG_GCJ
AC_PROG_INSTALL
AC_PROG_LN_S
AC_PROG_RANLIB
AC_PATH_PROG([ANT],[ant],[AC_MSG_ERROR([ant is required to build this.])])
AC_PATH_PROG([FSCKHFS],[fsck_hfs])
AC_PATH_PROG([FSTYPHFS],[fstyp_hfs])
AC_PATH_PROG([MOUNTHFS],[mount_hfs])
AC_PATH_PROG([NEWFSHFS],[newfs_hfs])

AX_PROG_JAVAH
AX_PROG_JAR
AX_JAVA_OPTIONS
AX_CHECK_JUNIT
AX_CHECK_JAVA_HOME
AX_PROG_JAVA_CC
AX_PROG_JAVAC
AX_PROG_JAVAC_WORKS
AX_PROG_JAVA
AX_PROG_JAVA_WORKS

# Checks for libraries.
AX_LIBGCJ_JAR

define([AC_LIBTOOL_LANG_CXX_CONFIG],[:])dnl
define([AC_LIBTOOL_LANG_F77_CONFIG],[:])dnl
LT_INIT
LT_LANG([Java])dnl

# Checks for header files.
AC_HEADER_STDBOOL dnl# also "_CHECK"s it
AC_CHECK_HEADERS([firefox/jni.h java/jni.h JavaVM/jni.h jni.h jni/jni.h \
                  malloc.h malloc/malloc.h stdio.h vm-jni.h \
                  windows.h windows/windows.h wine/windows/windows.h])dnl

# Checks for typedefs, structures, and compiler characteristics.
AC_C_CONST
AC_C_INLINE
AC_TYPE_SIZE_T

# Checks for library functions.
AC_FUNC_MALLOC

# Output.
AC_SUBST([GCJ_OPTS])dnl
AC_CONFIG_FILES([Makefile src.win32/llio/Makefile])
AC_OUTPUT
