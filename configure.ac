#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([hfsexplorer], [0_21])
AC_CONFIG_SRCDIR([src.win32/launcher/launcher.cpp])
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_MACRO_DIR([m4])
AC_CANONICAL_TARGET
AM_INIT_AUTOMAKE([foreign])
AM_MAINTAINER_MODE

# Checks for programs.
AC_PROG_CXX
AC_PROG_CC
AC_PROG_CPP
AM_PROG_GCJ
AC_PROG_INSTALL
AC_PROG_LN_S
AC_PATH_PROG([ANT], [ant], [AC_MSG_ERROR([ant is required to build this.])])

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

define([AC_LIBTOOL_LANG_CXX_CONFIG], [:])dnl
define([AC_LIBTOOL_LANG_F77_CONFIG], [:])dnl
LT_INIT
LT_LANG(Java)

# Checks for header files.
AC_CHECK_HEADERS([jni.h malloc.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_CHECK_HEADER_STDBOOL
AC_C_INLINE
AC_TYPE_SIZE_T

# Checks for library functions.
AC_FUNC_MALLOC

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
