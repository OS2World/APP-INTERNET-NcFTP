# Generated automatically from Makefile.in by configure.
#-----------------------------------------------------------------------------
#
# NcFTP sh_util makefile for the platform os/2, on the host neoiii.
#
#-----------------------------------------------------------------------------

CC=gcc
CFLAGS=-D_REENTRANT -D__EMX__ -DOS2 -D__ST_MT_ERRNO__ -g -Wno-format-y2k -static-libgcc
#CC=gcc
#CFLAGS=-O2 -W -Wall -Wstrict-prototypes -Wmissing-prototypes -Wmissing-declarations -Wshadow -Wbad-function-cast -Wwrite-strings -Wconversion
CPPFLAGS=-IU:/progetti/ncftp-3.2.5 -I../libncftp -I../Strn -I../sio -IU:/progetti/ncftp-3.2.5 -IU:/progetti/ncftp-3.2.5/libncftp -IU:/progetti/ncftp-3.2.5/sio -IU:/progetti/ncftp-3.2.5/Strn
prefix=/progetti/ncftp-3.2.5/os2
SYSCONFDIR=${prefix}/etc
SOCKS_LIBS=
LIBS= $(SOCKS_LIBS)
STRIP=: #strip
LDFLAGS=-L../libncftp -L../Strn -L../sio -LU:/progetti/ncftp-3.2.5/libncftp -LU:/progetti/ncftp-3.2.5/sio -LU:/progetti/ncftp-3.2.5/Strn -Zexe -Zomf -Zmap -Zargs-wild -D__ST_MT_ERRNO__

# Any -D definitions:
DEFS=-Dsh_util -DO_S=\"os/2\" -DSYSCONFDIR=\"$(SYSCONFDIR)\" -DHAVE_CONFIG_H

DPROGS=../bin/ncftpget.exe ../bin/ncftpput.exe ../bin/ncftpbatch.exe ../bin/ncftpls.exe

all: $(DPROGS)
	-@echo 'Done making NcFTP shell utilities.'

../bin/ncftpget.exe: ncftpget.c gpshare.o bookmark.o preffw.o spoolutil.o util.o gl_getline.o version.o gpshare.h syshdrs.h ../ncftp/util.h ../ncftp/pref.h ../ncftp/spool.h ../libncftp/ncftp.h ../libncftp/ncftp_errno.h ../libncftp/libncftp.a
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) gpshare.o bookmark.o preffw.o spoolutil.o util.o gl_getline.o version.o ncftpget.c -o ../bin/ncftpget.exe $(LDFLAGS) -lncftp -lStrn -lsio $(LIBS)
	-@$(STRIP) ../bin/ncftpget.exe

../bin/ncftpput.exe: ncftpput.c gpshare.o bookmark.o preffw.o spoolutil.o util.o gl_getline.o version.o gpshare.h syshdrs.h ../ncftp/util.h ../ncftp/pref.h ../ncftp/spool.h ../libncftp/ncftp.h ../libncftp/ncftp_errno.h ../libncftp/libncftp.a
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) gpshare.o bookmark.o preffw.o spoolutil.o util.o gl_getline.o version.o ncftpput.c -o ../bin/ncftpput.exe $(LDFLAGS) -lncftp -lStrn -lsio $(LIBS)
	-@$(STRIP) ../bin/ncftpput.exe

../bin/ncftpls.exe: ncftpls.c gpshare.o bookmark.o preffw.o util.o gl_getline.o version.o gpshare.h syshdrs.h ../ncftp/util.h ../ncftp/pref.h ../libncftp/ncftp.h ../libncftp/ncftp_errno.h ../libncftp/libncftp.a
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) gpshare.o bookmark.o preffw.o util.o gl_getline.o version.o ncftpls.c -o ../bin/ncftpls.exe $(LDFLAGS) -lncftp -lStrn -lsio $(LIBS)
	-@$(STRIP) ../bin/ncftpls.exe

../bin/ncftpbatch.exe: ncftpbatch.c preffw.o util.o spoolutil.o version.o gpshare.o bookmark.o ../ncftp/util.h ../ncftp/pref.h ../ncftp/spool.h gpshare.h syshdrs.h ../libncftp/ncftp.h ../libncftp/ncftp_errno.h ../libncftp/libncftp.a
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) preffw.o util.o spoolutil.o version.o gpshare.o bookmark.o ncftpbatch.c -o ../bin/ncftpbatch.exe $(LDFLAGS) -lncftp -lStrn -lsio $(LIBS)
	-@$(STRIP) ../bin/ncftpbatch.exe
	-@( cd ../bin ; rm -f ncftpspooler.exe ; ln -s ncftpbatch.exe ncftpspooler.exe )

util.o: ../ncftp/util.c ../ncftp/util.h syshdrs.h
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) -c ../ncftp/util.c

bookmark.o: ../ncftp/bookmark.c ../ncftp/bookmark.h syshdrs.h
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) -c ../ncftp/bookmark.c

gl_getline.o: ../ncftp/gl_getline.c ../ncftp/gl_getline.h syshdrs.h
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) -c ../ncftp/gl_getline.c

gpshare.o: gpshare.c gpshare.h syshdrs.h
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) -c gpshare.c

spool.o: ../ncftp/spool.c ../ncftp/spool.h syshdrs.h
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) -c ../ncftp/spool.c

spoolutil.o: ../ncftp/spoolutil.c ../ncftp/spool.h syshdrs.h
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) -c ../ncftp/spoolutil.c

preffw.o: ../ncftp/preffw.c ../ncftp/pref.h syshdrs.h
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) -c ../ncftp/preffw.c

version.o: ../ncftp/version.c
	$(CC) $(CFLAGS) $(DEFS) $(CPPFLAGS) ../ncftp/version.c -c

clean:
	/bin/rm -rf $(DPROGS) ../bin/ncftpspooler.exe *.o core *.pch SunWS_cache

PACKAGE=Makefile.in   gpshare.c     gpshare.h	  ncftpbatch.c \
	ncftpget.c    ncftpput.c    syshdrs.h	  ncftpls.c

TMPDIR=/tmp
TARDIR=sh_util

tarcp:
	-@mkdir -p $(TMPDIR)/TAR/$(TARDIR)
	-@chmod ga+r $(PACKAGE)
	-@chmod 755 $(TMPDIR)/TAR/$(TARDIR)
	cp -pr $(PACKAGE) $(TMPDIR)/TAR/$(TARDIR)
