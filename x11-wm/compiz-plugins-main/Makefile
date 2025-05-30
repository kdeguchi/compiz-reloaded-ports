PORTNAME=	compiz-plugins-main
PORTVERSION=	0.8.18
PORTREVISION=	4
CATEGORIES=	x11-wm

MAINTAINER=	freebsd-ports@dan.me.uk
COMMENT=	Plugins for Compiz Composite Window Manager
WWW=		https://github.com/compiz-reloaded

LICENSE=	GPLv2+
LICENSE_FILE=	${WRKSRC}/COPYING

BUILD_DEPENDS=	${LOCALBASE}/libdata/pkgconfig/compiz.pc:x11-wm/compiz \
		${LOCALBASE}/libdata/pkgconfig/bcop.pc:devel/compiz-bcop

LIB_DEPENDS=	libatspi.so:accessibility/at-spi2-core \
		libcairo.so:graphics/cairo \
		libdbus-1.so:devel/dbus \
		libpangocairo-1.0.so:x11-toolkits/pango \
		libstartup-notification-1.so:x11/startup-notification

RUN_DEPENDS=	compiz:x11-wm/compiz

USES=		autoreconf gl gmake gnome jpeg libtool localbase pathfix pkgconfig xorg

USE_GITLAB=	yes
GL_ACCOUNT=	compiz
GL_COMMIT=	0ea5db41983ba657481f87836c8d1f9498f8562a

USE_GL=	glu
USE_GNOME=	intltool
USE_LDCONFIG=	yes
USE_XORG=	ice sm x11 xcomposite xdamage xext xfixes xinerama xorgproto xrandr xrender

HAS_CONFIGURE=	yes
INSTALL_TARGET=	install-strip

OPTIONS_DEFINE=		NLS
OPTIONS_DEFAULT=	NLS
OPTIONS_SUB=	yes

NLS_USES=		gettext
NLS_CONFIGURE_ENABLE=	nls

.include <bsd.port.mk>
