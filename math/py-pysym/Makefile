PORTNAME=	pysym
DISTVERSION=	0.2.3
PORTREVISION=	4
CATEGORIES=	math python
MASTER_SITES=	PYPI
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Prototype package for symbolic manipulation
WWW=		https://github.com/bjodah/pysym

LICENSE=	BSD2CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}sympy>0:math/py-sympy@${PY_FLAVOR} \
		${PYNUMPY}

USES=		python
USE_PYTHON=	distutils autoplist
NO_ARCH=	yes

.include <bsd.port.mk>
