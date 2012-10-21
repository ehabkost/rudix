BuildRequires+=	/usr/local/lib/libevent.la

include ../../Library/GNU.mk

Title=		tmux
Name=		tmux
Version=	1.7
Revision=	0
URL=		http://downloads.sourceforge.net/tmux/
Source=		$(Name)-$(Version).tar.gz

ReadMeFile=	$(SourceDir)/NOTES
LicenseFile=	LICENSE

define test_inner_hook
$(BinDir)/tmux -V
endef
