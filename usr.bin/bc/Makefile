#	$OpenBSD: Makefile,v 1.10 2017/07/19 12:50:32 espie Exp $

.TOPDIR?=../..

PROG=		bc
SRCS=		bc.y scan.l tty.c dc.c bcode.c inout.c mem.c stack.c
CPPFLAGS+=	-I. -I${.CURDIR}
CPPFLAGS+=	-D'_PATH_LIBB="${SHAREDIR}/midc/bc.library"'
CPPFLAGS+=	-D'_PATH_DC="${bindir}/dc"'
CFLAGS+=	-Wall -Wno-unused
YFLAGS+=
LDADD+=		-ledit -lcurses -lcrypto
DPADD+=		${LIBEDIT} ${LIBCURSES} ${LIBCRYPTO}

# XXX: include add %/obj by default?
VPATH+=		${.CURDIR}/../dc

bc.c bc.h: bc.y
	${YACC} -o bc.c -d ${.CURDIR}/bc.y

scan.o: bc.h

beforeinstall:
	install -c -o ${BINOWN} -g ${BINGRP} -m 444 ${.CURDIR}/bc.library \
	    ${DESTDIR}/usr/share/misc

include ${.TOPDIR}/mk/bsd.prog.mk
