ACLOCAL_AMFLAGS = -I m4 --install

ant: build.xml
	@ANT@

all-local: ./buildall.sh
	$(MKDIR_P) ./dist/lib
	$(SHELL) -x ./buildall.sh 2>&1

all: ant buildall.sh all-local

.PHONY: all ant

SUBDIRS = src.win32/llio

DISTCLEANFILES = *~ autoscan.log m4/*~

distclean-local:
	-rm -rf .antbuild~ || rmdir .antbuild~
	-rm -rf autom4te.cache || rmdir autom4te.cache
