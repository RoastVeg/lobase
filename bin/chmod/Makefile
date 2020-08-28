#	$OpenBSD: Makefile,v 1.7 2001/09/06 18:52:55 mickey Exp $

.TOPDIR?=../..

PROG=	chmod
LDADD=	-lrt
MAN=	chmod.1 chgrp.1 chown.8 chflags.1
LINKS=	chmod ${DESTDIR}${BINDIR}/chgrp \
	chmod ${DESTDIR}${BINDIR}/chown

# XXX compatibility
afterinstall:
	(cd ${DESTDIR}/usr/sbin && \
	    ln -sf chown . && \
	    ln -sf chgrp . && \
	    chown -h ${BINOWN}:${BINGRP} chown chgrp)
	(cd ${DESTDIR}/usr/bin && \
	    ln -sf chmod chflags && \
	    chown -h ${BINOWN}:${BINGRP} chflags)

include ${.TOPDIR}/mk/bsd.prog.mk
