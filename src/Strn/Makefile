# Generated automatically from Makefile.in by configure.
#
# Strn makefile
#
VER=3.2.0
prefix=/progetti/ncftp-3.2.5/os2
MAN=${prefix}/man
SHELL=/bin/sh
.SUFFIXES: .c .o .so
LIB=libStrn.a
LIBSO=libStrn.so.1
LIBSOS=libStrn.so
CC=gcc
CPPFLAGS=-IU:/progetti/ncftp-3.2.5 -IU:/progetti/ncftp-3.2.5/libncftp -IU:/progetti/ncftp-3.2.5/sio -IU:/progetti/ncftp-3.2.5/Strn
#CFLAGS=-O2
CFLAGS=-D_REENTRANT -D__EMX__ -DOS2 -D__ST_MT_ERRNO__ -g -Wno-format-y2k -static-libgcc
DEFS=-DHAVE_CONFIG_H

DELETE=/bin/rm -rf
COPY=/bin/cp -pr
LIST=/bin/ls -l
MKDIR=mkdir -m 755 -p
SYMLINK=/bin/ln -s
HARDLINK=/bin/ln

CFILES=\
	DStrCat.c      DStrFree.c  Dynscpy.c	Strncpy.c   strtokc.c \
	DStrCatList.c  DStrInit.c  Dynsrecpy.c	Strnpcat.c  \
	DStrCpy.c      DStrNew.c   StrFree.c	Strnpcpy.c \
	DStrCpyList.c  Dynscat.c   Strncat.c	Strntok.c \
	Strncpy_NoZeroPad.c        Strncat_NoZeroPad.c

HFILES=\
	DStrInternal.h	Strn.h	   syshdrs.h

OBJS=\
	DStrCat.o      DStrFree.o  Dynscpy.o	Strncpy.o   strtokc.o \
	DStrCatList.o  DStrInit.o  Dynsrecpy.o	Strnpcat.o  \
	DStrCpy.o      DStrNew.o   StrFree.o	Strnpcpy.o \
	DStrCpyList.o  Dynscat.o   Strncat.o	Strntok.o \
	Strncpy_NoZeroPad.o        Strncat_NoZeroPad.o

SOBJS=\
	DStrCat.so      DStrFree.so  Dynscpy.so	Strncpy.so   strtokc.so \
	DStrCatList.so  DStrInit.so  Dynsrecpy.so  Strnpcat.so \
	DStrCpy.so      DStrNew.so   StrFree.so	Strnpcpy.so \
	DStrCpyList.so  Dynscat.so   Strncat.so	Strntok.so \
	Strncpy_NoZeroPad.so         Strncat_NoZeroPad.so

all: static
	-@echo "Done making Strn."

static: $(LIB)

$(LIB): $(OBJS)
	ar r $(LIB) $(OBJS)
	-@chmod 644 "$(LIB)"
	-echo "$(LIB)"
	-@echo "$(VER)" > Strn.version
	-@$(LIST) "$(LIB)"

.c.o:
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) $< -c

.c.so:
	$(CC) -fpic $(CFLAGS) $(CPPFLAGS) $(DEFS) $*.c -c -o $*.so

dynamic: $(LIBSO)

shared: $(LIBSO)

so: $(LIBSO)

$(LIBSO): $(SOBJS)
	$(DELETE) "$(LIBSO)" "$(LIBSOS)"
	$(CC) -shared "-Wl,-soname,$(LIBSO)" -o "$(LIBSO)" $(SOBJS)
	$(SYMLINK) "$(LIBSO)" "$(LIBSOS)"
	-@$(LIST) "$(LIBSOS)" "$(LIBSO)"

soinstall: $(LIBSO)
	$(COPY) "$(LIBSO)" "$(prefix)/lib/$(LIBSO)"
	( cd "$(prefix)/lib" ; $(SYMLINK) "$(LIBSO)" "$(LIBSOS)" )
	$(COPY) Strn.h "$(prefix)/include/Strn.h"
	-chmod a+r "$(prefix)/lib/$(LIBSO)" "$(prefix)/include/Strn.h"

tester: $(LIB) tester.c
	$(CC) $(CFLAGS) tester.c -o tester -I. -L. -lStrn

clean:
	$(DELETE) "$(LIB)" "$(LIBSO)" *.o *.so tester core *.pch SunWS_cache

distclean: clean
	-$(DELETE) config.h Makefile config.status config.cache config.log Strn.version

install_min:
	if test ! -d $(prefix)/include ; then $(MKDIR) "$(prefix)/include" ; fi
	if test ! -d $(prefix)/lib ; then $(MKDIR) "$(prefix)/lib" ; fi
	$(COPY) "$(LIB)" "$(prefix)/lib"
	-@echo "$(prefix)/lib/$(LIB)"
	$(COPY) Strn.h "$(prefix)/include/Strn.h"
	-chmod 664 "$(prefix)/include/Strn.h" "$(prefix)/lib/$(LIB)"

install:
	if test ! -d $(prefix)/include ; then $(MKDIR) "$(prefix)/include" ; fi
	if test ! -d $(prefix)/lib ; then $(MKDIR) "$(prefix)/lib" ; fi
	$(COPY) "$(LIB)" Strn.version "$(prefix)/lib"
	-@echo "$(prefix)/lib/$(LIB)"
	$(COPY) Strn.h "$(prefix)/include/Strn.h"
	-chmod 664 "$(prefix)/include/Strn.h" "$(prefix)/lib/Strn.version" "$(prefix)/lib/$(LIB)"
	-$(COPY) Strn.3 "$(MAN)/man3/Strn.3"
	-chmod 664 "$(MAN)/man3/Strn.3"
	-$(HARDLINK) "$(MAN)/man3/Strn.3" "$(MAN)/man3/Strncpy.3"
	-$(HARDLINK) "$(MAN)/man3/Strn.3" "$(MAN)/man3/Strncat.3"

uninstall:
	$(DELETE) "$(prefix)/lib/$(LIB)" "$(prefix)/include/Strn.h" "$(prefix)/lib/Strn.version"

PACKAGE=configure Makefile.in configure.in config.h.in Strn.vcproj Strn.sln tester.c $(CFILES) $(HFILES)

TMPDIR=/tmp
TARDIR=Strn
TARFILE=$(TARDIR).tar
TGZFILE=$(TARDIR).tgz

tarcp:
	-@$(MKDIR) $(TMPDIR)/TAR/$(TARDIR)
	-@chmod ga+r $(PACKAGE)
	-@chmod 755 $(TMPDIR)/TAR/$(TARDIR)
	$(COPY) $(PACKAGE) $(TMPDIR)/TAR/$(TARDIR)

tar: $(PACKAGE)
	-@$(MKDIR) $(TMPDIR)/TAR
	-@$(MKDIR) $(TMPDIR)/TAR/$(TARDIR)
	-@chmod ga+r $(PACKAGE)
	-@chmod 755 $(TMPDIR)/TAR/$(TARDIR)
	$(COPY) $(PACKAGE) $(TMPDIR)/TAR/$(TARDIR)
	( cd $(TMPDIR)/TAR ;  cvf $(TARFILE) ./$(TARDIR) )
	$(COPY) $(TMPDIR)/TAR/$(TARFILE) .
	-@chmod 644 $(TARFILE)
	-@$(DELETE) $(TMPDIR)/TAR
	-@$(LIST) $(TARFILE)

gz: tar
	gzip -c $(TARFILE) > $(TGZFILE)
	-@$(DELETE) $(TARFILE)
	-@chmod 644 $(TGZFILE)
	-@$(LIST) $(TGZFILE)

DStrCat.o: DStrCat.c Strn.h DStrInternal.h syshdrs.h
DStrCatList.o: DStrCatList.c Strn.h DStrInternal.h syshdrs.h
DStrCpy.o: DStrCpy.c Strn.h DStrInternal.h syshdrs.h
DStrCpyList.o: DStrCpyList.c Strn.h DStrInternal.h syshdrs.h
DStrFree.o: DStrFree.c Strn.h DStrInternal.h syshdrs.h
DStrInit.o: DStrInit.c Strn.h DStrInternal.h syshdrs.h
DStrNew.o: DStrNew.c Strn.h DStrInternal.h syshdrs.h
Dynscpy.o: Dynscpy.c Strn.h syshdrs.h
Dynscat.o: Dynscat.c Strn.h syshdrs.h
Strncat.o: Strncat.c Strn.h syshdrs.h
Strncpy.o: Strncpy.c Strn.h syshdrs.h
Strnpcat.o: Strnpcat.c Strn.h syshdrs.h
Strnpcpy.o: Strnpcpy.c Strn.h syshdrs.h
Strntok.o: Strntok.c Strn.h syshdrs.h
strtokc.o: strtokc.c Strn.h syshdrs.h
Strncpy_NoZeroPad.o: Strncpy_NoZeroPad.c Strn.h syshdrs.h
Strncat_NoZeroPad.o: Strncat_NoZeroPad.c Strn.h syshdrs.h
