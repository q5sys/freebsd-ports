PORTNAME=	SparseBitSet
PORTVERSION=	1.3
CATEGORIES=	devel java
MASTER_SITES=	https://repo1.maven.org/maven2/com/zaxxer/${PORTNAME}/${PORTVERSION}/
EXTRACT_SUFX=	.jar
EXTRACT_ONLY=

MAINTAINER=	thierry@FreeBSD.org
COMMENT=	Efficient sparse bitset implementation for Java
WWW=		https://github.com/brettwooldridge/SparseBitSet

LICENSE=	APACHE20

USES=		java

NO_BUILD=	yes
NO_ARCH=	yes

PLIST_FILES=	${JAVAJARDIR}/${PORTNAME}.jar

do-install:
	@${MKDIR} ${STAGEDIR}${JAVAJARDIR}
	${INSTALL_DATA} ${DISTDIR}/${DISTFILES}	\
		${STAGEDIR}${JAVAJARDIR}/${PORTNAME}.jar

.include <bsd.port.mk>
