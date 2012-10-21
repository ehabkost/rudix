BuildRequires+=	/usr/local/lib/libevent.la

include ../../Library/GNU.mk

Title=		tmux
Name=		tmux
Version=	1.7
Revision=	0
URL=		http://sourceforge.net/projects/$(Name)/files/$(Name)/$(Name)-$(Version)
Source=		$(Name)-$(Version).tar.gz

ReadMeFile=	$(SourceDir)/NOTES
LicenseFile=	LICENSE

# FIXME: workaround to avoid 'curses not found'
define build_inner_hook
$(call info_color,Running Configure)
cd $(BuildDir) ; \
env CFLAGS="-arch i386 -arch x86_64" $(configure) --disable-dependency-tracking
$(call info_color,Done)
cd $(BuildDir) ; $(make) $(MakeExtra)
endef

define test_inner_hook
$(BinDir)/tmux -V
endef
