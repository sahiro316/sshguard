SUBDIRS = common blocker fw parser

EXTRA_DIST = sshguard.in

dist_libexec_SCRIPTS = sshg-logtail
sbin_SCRIPTS = sshguard

CLEANFILES = sshguard

script_subst = sed \
	-e 's|@libexecdir[@]|$(libexecdir)|g' \
	-e 's|@sysconfdir[@]|$(sysconfdir)|g' \
	-e 's|@sshguardversion[@]|$(VERSION)|g'

sshguard: Makefile sshguard.in
	$(script_subst) $(srcdir)/$@.in > $@
