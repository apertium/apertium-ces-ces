AC_PREREQ(2.52)

AC_INIT([Apertium Czech-Czech], [0.1.0], [awesomeevildudes@gmail.com], [apertium-ces-ces], [https://wiki.apertium.org/wiki/Apertium-ces-ces])
AM_INIT_AUTOMAKE
AC_PROG_AWK

PKG_CHECK_MODULES(APERTIUM, apertium >= 3.6.1)
PKG_CHECK_MODULES(LTTOOLBOX, lttoolbox >= 3.5.1)



AC_PATH_PROGS(ZCAT, [gzcat zcat], [false])
AS_IF([test x$ZCAT = xfalse], [AC_MSG_ERROR([You don't have zcat nor gzcat installed])])

m4_ifdef([AP_CHECK_LING],[],[AC_MSG_ERROR([AP_CHECK_LING not defined, is apertium.m4 in ACLOCAL_PATH? See: https://wiki.apertium.org/wiki/Installation_troubleshooting])])


PKG_CHECK_MODULES(REGTEST, apertium-regtest >= 0.0.1, [],
                  [AC_MSG_WARN([Running tests requires apertium-regtest])])

AP_MKINCLUDE

AC_OUTPUT([Makefile])
