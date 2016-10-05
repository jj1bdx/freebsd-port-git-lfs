# $FreeBSD: head/devel/git-lfs/Makefile 423051 2016-10-01 10:55:40Z antoine $

PORTNAME=	git-lfs
PORTVERSION=	1.4.1
DISTVERSIONPREFIX=	v
CATEGORIES=	devel
MASTER_SITES=	GH GHC
PKGNAMEPREFIX=	go-

MAINTAINER=	kuriyama@FreeBSD.org
COMMENT=	Git extension for versioning large files

LICENSE=	MIT

#BROKEN=		fails to build
DEPRECATED=	Broken for more than 6 months
EXPIRATION_DATE=	2016-11-01

USES=		go
USE_GITHUB=	yes
GH_ACCOUNT=	github
PLIST_FILES=	bin/git-lfs

GO_PKGNAME=	github.com/${GH_ACCOUNT}/${PORTNAME}

# see https://github.com/github/git-lfs/wiki/Installation

do-build:
	cd ${WRKSRC} && script/bootstrap

pre-install:
	${INSTALL_PROGRAM} ${WRKSRC}/bin/git-lfs ${STAGEDIR}${PREFIX}/bin/git-lfs

.include <bsd.port.mk>
