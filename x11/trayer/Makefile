PORTNAME=	trayer
PORTVERSION=	1.1.8
DISTVERSIONPREFIX=	${PORTNAME}-
PORTREVISION=	2
CATEGORIES=	x11

MAINTAINER=	madpilot@FreeBSD.org
COMMENT=	Lightweight GTK2-based systray for UNIX desktop
WWW=		https://github.com/sargon/trayer-srg

LIB_DEPENDS=	libfontconfig.so:x11-fonts/fontconfig \
		libfreetype.so:print/freetype2

USES=		iconv gmake gnome pkgconfig xorg
USE_GNOME=	atk cairo gdkpixbuf glib20 gtk20 pango
USE_GITHUB=	yes
USE_XORG=	x11 xmu
HAS_CONFIGURE=	yes
CONFIGURE_ARGS=	--prefix="${PREFIX}"

GH_ACCOUNT=	sargon
GH_PROJECT=	${PORTNAME}-srg

PORTDOCS=	README CREDITS CHANGELOG

PLIST_FILES=	bin/trayer share/man/man1/trayer.1.gz

OPTIONS_DEFINE=	DOCS

post-install:
	${INSTALL_MAN} ${WRKSRC}/man/${PORTNAME}.1 ${STAGEDIR}${PREFIX}/share/man/man1
	${MKDIR} ${STAGEDIR}${DOCSDIR}
.for f in ${PORTDOCS}
	${INSTALL_DATA} ${WRKSRC}/${f} ${STAGEDIR}${DOCSDIR}
.endfor

.include <bsd.port.mk>
