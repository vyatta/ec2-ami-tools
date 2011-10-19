# Put files in the same locations as does the corresponding ubuntu package.
#

bindir = /usr/bin
etcdir = /etc
libdir = /usr/lib/ec2-ami-tools/lib

toolsdir = ec2-ami-tools-1.4.0.1

cpiop = find  . ! -regex '\(.*~\|.*\.bak\|.*\.swp\|.*\#.*\#\)' -print0 | \
  cpio -0pd

install-exec-hook:
	mkdir -p $(DESTDIR)$(bindir)
	cd $(toolsdir)/bin; $(cpiop) $(DESTDIR)$(bindir)
	mkdir -p $(DESTDIR)$(etcdir)
	cd $(toolsdir)/etc; $(cpiop) $(DESTDIR)$(etcdir)
	mkdir -p $(DESTDIR)$(libdir)
	cd $(toolsdir)/lib; $(cpiop) $(DESTDIR)$(libdir)



