## Process this file with automake to generate Makefile.in.

LIBS = 
INCLUDES = -I$(top_srcdir)/include

noinst_LTLIBRARIES = libsections.la


## All source files used when building this submodule, including all
## headers.

SectionsSources = \
	BlocksSection.cpp BlocksSection.h \
	ClassesSection.cpp ClassesSection.h \
	EntitiesSection.cpp EntitiesSection.h \
	HeaderSection.cpp HeaderSection.h \
	ObjectsSection.cpp ObjectsSection.h \
	Section.cpp Section.h \
	TablesSection.cpp TablesSection.h \
	UnknownSection.cpp UnknownSection.h

libsections_la_SOURCES = \
	$(SectionsSources)

## Installation information.

libsectionsincdir = $(includedir)/dime/sections
libsectionsinc_HEADERS = \
	../../include/dime/sections/BlocksSection.h \
	../../include/dime/sections/ClassesSection.h \
	../../include/dime/sections/EntitiesSection.h \
	../../include/dime/sections/HeaderSection.h \
	../../include/dime/sections/ObjectsSection.h \
	../../include/dime/sections/Section.h \
	../../include/dime/sections/TablesSection.h \
	../../include/dime/sections/UnknownSection.h

install-libsectionsincHEADERS: $(libsectionsinc_HEADERS)
	@$(NORMAL_INSTALL)
	$(mkinstalldirs) $(DESTDIR)$(libsectionsincdir)
	@list='$(libsectionsinc_HEADERS)'; for p in $$list; do \
	  if test -f "$$p"; then d= ; else d="$(srcdir)/"; fi; \
	  f="`echo $$p | sed -e 's|^.*/||'`"; \
	  echo " $(INSTALL_DATA) $$d$$p $(DESTDIR)$(libsectionsincdir)/$$f"; \
	  $(INSTALL_DATA) $$d$$p $(DESTDIR)$(libsectionsincdir)/$$f; \
	done

uninstall-libsectionsincHEADERS:
	@$(NORMAL_UNINSTALL)
	@list='$(libsectionsinc_HEADERS)'; for p in $$list; do \
	  f="`echo $$p | sed -e 's|^.*/||'`"; \
	  echo " rm -f $(DESTDIR)$(libsectionsincdir)/$$f"; \
	  rm -f $(DESTDIR)$(libsectionsincdir)/$$f; \
	done

