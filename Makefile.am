ACLOCAL_AMFLAGS = -I aclocal
ACLOCAL_FILES = aclocal/version.m4 aclocal/ax_create_stdint_h.m4
AM_CFLAGS = -Wall

bin_PROGRAMS = prxtool

TINYXML = $(srcdir)/tinyxml
INLCUDES = -I $(srcdir) -I $(TINYXML) $(CAPSTONE_CFLAGS) $(YAML_CFLAGS)

LIBS = $(CAPSTONE_LIBS) $(JANSSON_LIBS) $(YAML_LIBS)

prxtool_SOURCES = \
	main.C \
	ProcessElf.C \
	ProcessPrx.C \
	NidMgr.C \
	VirtualMem.C \
	output.C \
	SerializePrx.C \
	SerializePrxToIdc.C \
	SerializePrxToXml.C \
	SerializePrxToMap.C \
	pspkerror.C \
	disasm.C \
	getargs.C \
	$(TINYXML)/tinyxml.cpp \
	$(TINYXML)/tinyxmlparser.cpp \
	$(TINYXML)/tinystr.cpp \
	$(TINYXML)/tinyxmlerror.cpp \
	vita-import.c \
	yamltree.c \
	yamltreeutil.c

noinst_HEADERS = \
	types.h \
	elftypes.h \
	prxtypes.h \
	output.h \
	NidMgr.h \
	ProcessElf.h \
	ProcessPrx.h \
	SerializePrx.h \
	SerializePrxToIdc.h \
	SerializePrxToXml.h \
	SerializePrxToMap.h \
	VirtualMem.h \
	pspkerror.h \
	disasm.h \
	getargs.h \
	$(TINYXML)/tinystr.h \
	$(TINYXML)/tinyxml.h \
	vita-import.h \
	yamltree.h \
	yamltreeutil.h

EXTRA_DIST = \
	$(ACLOCAL_FILES) \
	LICENSE \
	$(TINYXML)/VERSION \
	$(TINYXML)/changes.txt \
	$(TINYXML)/readme.txt

DISTCLEANFILES = _stdint.h
