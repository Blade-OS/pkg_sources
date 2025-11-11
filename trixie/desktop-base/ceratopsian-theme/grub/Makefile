dir = usr/share/desktop-base/ceratopsian-theme/grub

.PHONY: build clean install

install:
	install -d $(DESTDIR)/$(dir)
	$(INSTALL_DATA) $(wildcard *.png *.sh) $(DESTDIR)/$(dir)

include ../../Makefile.inc
