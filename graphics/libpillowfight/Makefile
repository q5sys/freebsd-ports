PORTNAME=	libpillowfight
DISTVERSION=	0.3.1
CATEGORIES=	graphics python

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Library containing various image processing algorithms
WWW=		https://gitlab.gnome.org/World/OpenPaperwork/libpillowfight

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	gmake:devel/gmake
TEST_DEPENDS=	gmake:devel/gmake \
		tox:devel/py-tox@${PY_FLAVOR}

USES=		cmake python:test
USE_LDCONFIG=	yes

USE_GITLAB=	yes
GL_SITE=	https://gitlab.gnome.org/World
GL_ACCOUNT=	OpenPaperwork
GL_TAGNAME=	254018aad15710af6e9bdc5eb61aaa7dbac6f747

PLIST_FILES=	include/pillowfight/pillowfight.h \
		include/pillowfight/util.h \
		lib/libpillowfight.so \
		lib/libpillowfight.so.0

pre-configure:
	@cd ${WRKSRC} && ${GMAKE} version

do-test: # many tests fail due to various reasons: https://gitlab.gnome.org/World/OpenPaperwork/libpillowfight/issues/18#note_279228
	@cd ${WRKSRC} && ${GMAKE} test

.include <bsd.port.mk>
