# Generated automatically from Makefile.in by configure.
#-----------------------------------------------------------------------------
#
# NcFTP vis makefile for the platform os/2, on the host neoiii.
#
#-----------------------------------------------------------------------------

CC=gcc
CFLAGS=-D_REENTRANT -D__EMX__ -DOS2 -D__ST_MT_ERRNO__ -g -Wno-format-y2k -static-libgcc
#CC=gcc
#CFLAGS=-O2 -W -Wall -Wstrict-prototypes -Wmissing-prototypes -Wmissing-declarations -Wshadow -Wbad-function-cast -Wwrite-strings -Wconversion
CPPFLAGS=-IU:/progetti/ncftp-3.2.5 -I../libncftp -I../Strn -I../sio -IU:/progetti/ncftp-3.2.5 -IU:/progetti/ncftp-3.2.5/libncftp -IU:/progetti/ncftp-3.2.5/sio -IU:/progetti/ncftp-3.2.5/Strn
prefix=/progetti/ncftp-3.2.5/os2
exec_prefix=${prefix}
BINDIR=${exec_prefix}/bin
SYSCONFDIR=${prefix}/etc
SOCKS_LIBS=
CURSESLIBS=
LIBS=$(CURSESLIBS)  $(SOCKS_LIBS)
STRIP=: #strip
LDFLAGS=-L../libncftp -L../Strn -L../sio -LU:/progetti/ncftp-3.2.5/libncftp -LU:/progetti/ncftp-3.2.5/sio -LU:/progetti/ncftp-3.2.5/Strn -Zexe -Zomf -Zmap -Zargs-wild -D__ST_MT_ERRNO__

# Any -D definitions:
DEFS=-Dvis -DO_S=\"os/2\" -DNCFTPPATH=\"$(BINDIR)/ncftp\" -DSYSCONFDIR=\"$(SYSCONFDIR)\" -DHAVE_CONFIG_H

DPROGS=# ../bin/ncftpbookmarks.exe

all: $(DPROGS)
	-@echo 'Done making NcFTP full-screen utilities.'

../bin/ncftpbookmarks.exe: bmed.c wgets.o wutil.o pref.o preffw.o trace.o util.o bookmark.o version.o bmed.h wgets.h syshdrs.h ../libncftp/libncftp.a
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) bmed.c wgets.o wutil.o pref.o preffw.o trace.o util.o bookmark.o version.o -o ../bin/ncftpbookmarks.exe $(LDFLAGS) -lncftp -lStrn -lsio $(LIBS)
	-@$(STRIP) ../bin/ncftpbookmarks.exe
	-@/bin/rm -rf ../bin/ncftpbookmarks.dSYM

bookmark.o: ../ncftp/bookmark.c ../ncftp/bookmark.h syshdrs.h
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) ../ncftp/bookmark.c -c

pref.o: ../ncftp/pref.c ../ncftp/pref.h syshdrs.h
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) ../ncftp/pref.c -c

preffw.o: ../ncftp/preffw.c ../ncftp/pref.h syshdrs.h
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) ../ncftp/preffw.c -c

trace.o: ../ncftp/trace.c ../ncftp/trace.h syshdrs.h
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) ../ncftp/trace.c -c

util.o: ../ncftp/util.c ../ncftp/util.h syshdrs.h
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) ../ncftp/util.c -c

version.o: ../ncftp/version.c
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) ../ncftp/version.c -c

wutil.o: wutil.c wutil.h syshdrs.h
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) wutil.c -c

wgets.o: wgets.c wgets.h syshdrs.h
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) wgets.c -c

clean:
	/bin/rm -rf $(DPROGS) *.o core *.pch SunWS_cache

PACKAGE=Makefile.in bmed.c bmed.h syshdrs.h wgets.c wgets.h wutil.c wutil.h

TMPDIR=/tmp
TARDIR=vis

tarcp:
	-@mkdir -p $(TMPDIR)/TAR/$(TARDIR)
	-@chmod ga+r $(PACKAGE)
	-@chmod 755 $(TMPDIR)/TAR/$(TARDIR)
	cp -pr $(PACKAGE) $(TMPDIR)/TAR/$(TARDIR)
