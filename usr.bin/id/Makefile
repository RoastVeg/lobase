#	$OpenBSD: Makefile,v 1.5 2013/09/06 19:48:46 okan Exp $

.TOPDIR?=../..

PROG=	id
MAN=	id.1 groups.1 whoami.1

LINKS=	id ${DESTDIR}${BINDIR}/groups \
	id ${DESTDIR}${BINDIR}/whoami

include ${.TOPDIR}/mk/bsd.prog.mk
