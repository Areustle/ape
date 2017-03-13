#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([ape],[1.0])
AC_CONFIG_AUX_DIR([aux])
AC_CONFIG_MACRO_DIR([m4])

AM_INIT_AUTOMAKE([foreign -Wall -Werror])
AM_MAINTAINER_MODE([enable])
AM_PROG_AR

LT_PREREQ([2.2])
LT_INIT([disable-static])

AC_CONFIG_FILES([Makefile
                 src/Makefile
                 src/pcheck/Makefile
                 src/pget/Makefile
                 src/plist/Makefile
                 src/pquery/Makefile
                 src/pquery2/Makefile
                 src/pset/Makefile
                 src/punlearn/Makefile
                 include/ape/Makefile])
                 # src/test/Makefile

AC_CONFIG_SRCDIR([src/pil_error.c])

# Checks for programs.
AC_PROG_CC
AM_PROG_CC_C_O

# Checks for libraries.
AC_SEARCH_LIBS([clear_history] , [readline] ,
               [AC_DEFINE([USE_READLINE],[1],[Enable Readline])],
               [AC_MSG_ERROR([required program 'readline' not found.])])

# Checks for header files.
AC_CHECK_HEADERS([float.h limits.h malloc.h stddef.h stdlib.h string.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_TYPE_SIZE_T

# Checks for library functions.
AC_FUNC_MALLOC
AC_FUNC_STRTOD
AC_CHECK_FUNCS([atexit gethostname memchr memset setenv strchr strrchr strstr strtol])

AC_OUTPUT
