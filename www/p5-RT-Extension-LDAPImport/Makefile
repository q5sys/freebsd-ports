PORTNAME=	RT-Extension-LDAPImport
PORTVERSION=	0.36
PORTREVISION=	5
CATEGORIES=	www net perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	perl@FreeBSD.org
COMMENT=	RT extension to import users from an LDAP store
WWW=		https://metacpan.org/release/RT-Extension-LDAPImport

LICENSE=	ART10 GPLv1+
LICENSE_COMB=	dual

BUILD_DEPENDS=	${RUN_DEPENDS}
RUN_DEPENDS=	p5-perl-ldap>0:net/p5-perl-ldap \
		p5-Class-Accessor>0:devel/p5-Class-Accessor \
		${LOCALBASE}/bin/rt:www/rt${RT_VER}

RT_VER=		44

USES+=		perl5
USE_PERL5=	configure

NO_ARCH=	yes

PLIST_SUB+=	RTHOME=share/rt${RT_VER}

post-patch:
		@${REINPLACE_CMD} -e 's|LocalPath/man/man3|LocalPath/share/man/man3|g' ${WRKSRC}/inc/Module/Install/RTx.pm

# Note: You can install using an arbitrary $PREFIX but only if it
# matches the $PREFIX used to install www/rt44.  Hence ignore
# $PREFIX in the environment and inherit settings from RT.pm
do-configure:
	@cd ${CONFIGURE_WRKSRC} && \
	    unset PREFIX && \
	    ${SETENV} ${CONFIGURE_ENV} ${PERL5} -I${SITE_PERL} ${CONFIGURE_CMD} && \
	    ${PERL5} -pi -e 's/ doc_(perl|site|\$$\(INSTALLDIRS\))_install$$//' Makefile

post-configure:
	${REINPLACE_CMD} "/RTxPlugin/d" ${WRKSRC}/Makefile

post-install:
	${RM} ${STAGEDIR}${PREFIX}/man/auto/RT/Extension/LDAPImport/.packlist
	${RMDIR} -p ${STAGEDIR}${PREFIX}/man/auto/RT/Extension/LDAPImport 2>/dev/null || :

.include <bsd.port.mk>
