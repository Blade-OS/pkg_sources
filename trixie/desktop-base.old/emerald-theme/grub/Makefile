dir = usr/share/desktop-base/emerald/grub

.PHONY: build clean install

files = \
	background.png

build: $(files)

install:
	install -d $(DESTDIR)/$(dir)
	$(INSTALL_DATA) $(wildcard *.png *.sh) $(DESTDIR)/$(dir)

background.png: background.svg
	inkscape --export-filename=$@ $<
	mv $@ $@.raw
	optipng $@.raw -out $@

include ../../Makefile.inc
