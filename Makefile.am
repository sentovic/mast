AUTOMAKE_OPTIONS = foreign

BUILT_SOURCES = VERSION

VERSION: configure.ac
	echo "${PACKAGE_NAME}" > VERSION; \
	echo "${PACKAGE_VERSION}" >> VERSION

SUBDIRS = src doc
EXTRA_DIST = VERSION autogen.sh

# Copy README.md to README when building distribution
dist-hook:
	[ -f README.md ] && cat README.md > README || true
	[ -f NEWS.md ] && cat NEWS.md > NEWS || true
