#	$OpenBSD: Makefile,v 1.7 2016/03/30 06:38:46 jmc Exp $

.TOPDIR?=../..

PROG=	grep
SRCS=	binary.c file.c grep.c mmfile.c queue.c util.c
LINKS=	grep ${DESTDIR}${BINDIR}/egrep \
	grep ${DESTDIR}${BINDIR}/fgrep \
	grep ${DESTDIR}${BINDIR}/zgrep \
	grep ${DESTDIR}${BINDIR}/zegrep \
	grep ${DESTDIR}${BINDIR}/zfgrep \

CFLAGS+= -Wall

LDADD=	-lz
DPADD=	${LIBZ}

include ${.TOPDIR}/mk/bsd.prog.mk
