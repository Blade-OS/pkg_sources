dir = usr/share/desktop-base/ceratopsian-theme/grub

.PHONY: build clean install

files = \
	background.png

build: $(files)

clean:
	rm -f background.png.raw
	rm -f background.png

install:
	install -d $(DESTDIR)/$(dir)
	$(INSTALL_DATA) $(wildcard *.png *.sh) $(DESTDIR)/$(dir)

wallpaper.png: wallpaper.svg
	inkscape --export-filename=$@ $<
	mv $@ $@.raw
	optipng $@.raw -out $@

include ../../Makefile.inc
