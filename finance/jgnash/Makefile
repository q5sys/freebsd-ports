PORTNAME=	jgnash
PORTVERSION=	2.21.0
CATEGORIES=	finance java
MASTER_SITES=	SF/jgnash/Active%20Stable%202.x
DISTNAME=	jgnash-${PORTVERSION}-bin

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Free personal finance manager
WWW=		https://sourceforge.net/projects/jgnash/

LICENSE=	GPLv3

WRKSRC=		${WRKDIR}/jgnash-${PORTVERSION}
DATADIR=	${JAVASHAREDIR}/${PORTNAME}
SUB_FILES=	jgnash.desktop
SUB_LIST=	JAVA="${JAVA}"
PLIST_SUB+=	DESKTOPDIR=${DESKTOPDIR:S|^${PREFIX}/||}

USES=		java zip
JAVA_VENDOR=	openjdk

NO_BUILD=	yes
NO_ARCH=	yes

do-install:
	@${MKDIR} ${STAGEDIR}${DATADIR}
	@${CP} ${WRKSRC}/jgnash2.jar ${STAGEDIR}${DATADIR}
	@${CP} -R ${WRKSRC}/lib ${STAGEDIR}${DATADIR}
	@${CP} ${WRKDIR}/jgnash.desktop ${STAGEDIR}${DESKTOPDIR}

.include <bsd.port.mk>
