PORTNAME=	rnc2rng
DISTVERSION=	2.7.0
PORTREVISION=	1
CATEGORIES=	textproc python
MASTER_SITES=	PYPI
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	RELAX NG Compact to regular syntax conversion library
WWW=		https://github.com/djc/rnc2rng

LICENSE=	MIT

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}rply>0:devel/py-rply@${PY_FLAVOR}

USES=		python
USE_PYTHON=	distutils concurrent autoplist
NO_ARCH=	yes

.include <bsd.port.mk>
