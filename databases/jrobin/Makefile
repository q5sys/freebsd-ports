PORTNAME=	jrobin
PORTVERSION=	1.5.14
CATEGORIES=	databases java
MASTER_SITES=	SF
EXTRACT_SUFX=	.jar
EXTRACT_ONLY=

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Pure Java alternative to RRDTool
WWW=		http://www.jrobin.org/

USES=		java
NO_BUILD=	yes

CLASSES=	jrobin

do-install:
.for c in ${CLASSES}
	${INSTALL_DATA} ${DISTDIR}/${c}-${PORTVERSION}.jar ${STAGEDIR}${JAVAJARDIR}/${c}.jar
	@${ECHO} '${JAVAJARDIR:S,^${PREFIX}/,,}/${c}.jar' >> ${TMPPLIST}
.endfor

.include <bsd.port.mk>
