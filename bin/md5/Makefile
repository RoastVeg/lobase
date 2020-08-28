#	$OpenBSD: Makefile,v 1.15 2016/03/30 06:38:40 jmc Exp $

.TOPDIR?=../..

PROG=	md5
SRCS=	crc.c md5.c
MAN=	cksum.1 md5.1
LINKS=	md5 ${DESTDIR}${BINDIR}/sha1 \
	md5 ${DESTDIR}${BINDIR}/sha256 \
	md5 ${DESTDIR}${BINDIR}/sha512 \
	md5 ${DESTDIR}${BINDIR}/cksum

CPPFLAGS+= -I${.CURDIR}
COPTS+=	-Wall -Wconversion -Wmissing-prototypes

include ${.TOPDIR}/mk/bsd.prog.mk
