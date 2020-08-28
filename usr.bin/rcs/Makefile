#	$OpenBSD: Makefile,v 1.40 2010/10/15 08:44:12 tobias Exp $

.TOPDIR?=../..

PROG=	rcs
MAN=	ci.1 co.1 ident.1 merge.1 rcs.1 rcsclean.1 rcsdiff.1 rcsmerge.1 rlog.1

SRCS=	ci.c co.c ident.c merge.c rcsclean.c rcsdiff.c rcsmerge.c rcsparse.c \
	rcsprog.c rlog.c rcsutil.c buf.c date.y diff.c diff3.c rcs.c rcsnum.c \
	rcstime.c worklist.c xmalloc.c

LINKS=	rcs ${DESTDIR}${BINDIR}/ci rcs ${DESTDIR}${BINDIR}/co \
	rcs ${DESTDIR}${BINDIR}/ident rcs ${DESTDIR}${BINDIR}/merge \
	rcs ${DESTDIR}${BINDIR}/rcsclean rcs ${DESTDIR}${BINDIR}/rcsdiff \
	rcs ${DESTDIR}${BINDIR}/rcsmerge rcs ${DESTDIR}${BINDIR}/rlog

CPPFLAGS+=-I${.CURDIR}
CFLAGS+=-Wall
CFLAGS+=-Wstrict-prototypes -Wmissing-prototypes
CFLAGS+=-Wmissing-declarations
CFLAGS+=-Wshadow -Wpointer-arith -Wcast-qual
CFLAGS+=-Wsign-compare
YFLAGS=

include ${.TOPDIR}/mk/bsd.prog.mk
