PORTNAME=	npretty
DISTVERSIONPREFIX=	n
DISTVERSION=	0.9.3-1
PORTREVISION=	5
CATEGORIES=	graphics

MAINTAINER=	peter@pean.org
COMMENT=	Simple web-gallery generator written in perl
WWW=		http://www.pulia.nu/coding.html

LICENSE=	GPLv2

RUN_DEPENDS=	p5-Image-ExifTool>=0:graphics/p5-Image-ExifTool \
		p5-forks>=0:devel/p5-forks

USE_GITHUB=	yes
GH_ACCOUNT=	gammy

NO_BUILD=	yes
USES=		magick:6 perl5 shebangfix
USE_PERL5=	run
SHEBANG_FILES=	npretty.pl

OPTIONS_DEFINE=	DOCS

post-patch:
	@ ${REINPLACE_CMD} -e "s|/etc/|${PREFIX}/etc/|" ${WRKSRC}/npretty.pl

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/npretty.pl ${STAGEDIR}${PREFIX}/bin
	@${MKDIR} ${STAGEDIR}${PREFIX}/etc/npretty
	${INSTALL_DATA} ${WRKSRC}/novideo.gif ${STAGEDIR}${PREFIX}/etc/npretty
	${INSTALL_DATA} ${WRKSRC}/npretty_template.tpl ${STAGEDIR}${PREFIX}/etc/npretty
	${INSTALL_DATA} ${WRKSRC}/npretty.conf ${STAGEDIR}${PREFIX}/etc/npretty
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
.for f in BUGS README
	${INSTALL_DATA} ${WRKSRC}/${f} ${STAGEDIR}${DOCSDIR}
.endfor

.include <bsd.port.mk>
