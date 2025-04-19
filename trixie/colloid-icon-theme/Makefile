# Package details
PACKAGE_NAME = colloid-icon-theme
THEME_DIR = theme
DEB_PACKAGE = $(PACKAGE_NAME)_$(PACKAGE_VERSION)_$(PACKAGE_ARCH).deb

# Directories for packaging
DEBIAN_DIR = ./debian
SRC_DIR = ./src

# Prepare build directories
prepare:
	@echo "Setting up directories for the package..."
	mkdir -p $(SRC_DIR)/usr/share/colloid-installer

	@echo "Copying theme installer..."
	cp -r $(THEME_DIR)/* $(SRC_DIR)/usr/share/colloid-installer/

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

.PHONY: all prepare deb clean
