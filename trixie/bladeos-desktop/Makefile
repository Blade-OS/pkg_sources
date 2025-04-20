# Package details
PACKAGE_NAME = bladeos-desktop
GNOME_DIR = usr/share/gnome-shell
DEB_PACKAGE = $(PACKAGE_NAME)_$(PACKAGE_VERSION)_$(PACKAGE_ARCH).deb

# Directories for packaging
DEBIAN_DIR = ./debian
SRC_DIR = ./src

# Prepare build directories
prepare:
	@echo "Setting up directories for the package..."
	mkdir -p $(SRC_DIR)/usr/share/gnome-shell/extensions

	@echo "Copying GNOME extension..."
	cp -r $(GNOME_DIR)/* $(SRC_DIR)/usr/share/gnome-shell/

# Build the source and binary package using dpkg-buildpackage
deb: prepare
	@echo "Building the .deb package..."
	dpkg-buildpackage -us -uc

	@echo "Package created: $(DEB_PACKAGE)"

# Clean build artifacts
clean:
	@echo "Cleaning build files..."
	rm -rf $(SRC_DIR)/*
	rm -f $(DEB_PACKAGE)
	rm -rf $(DEBIAN_DIR)/$(PACKAGE_NAME)

.PHONY: all prepare deb clean
