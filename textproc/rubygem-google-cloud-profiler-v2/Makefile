PORTNAME=	google-cloud-profiler-v2
PORTVERSION=	0.9.1
PORTREVISION=	1
CATEGORIES=	textproc rubygems
MASTER_SITES=	RG

MAINTAINER=	mfechner@FreeBSD.org
COMMENT=	Ruby Client to manage continous progiling information
WWW=		https://github.com/googleapis/google-cloud-ruby/tree/main/google-cloud-profiler-v2

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE.md

RUN_DEPENDS=	rubygem-gapic-common-gitlab>=0.21.1<2:devel/rubygem-gapic-common-gitlab \
		rubygem-google-cloud-errors>=1.0<2:net/rubygem-google-cloud-errors

USES=		gem

NO_ARCH=	yes

.include <bsd.port.mk>
