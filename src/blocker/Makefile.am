AM_CFLAGS=-I$(top_srcdir)/src/common -DSIMCLIST_NO_DUMPRESTORE

libexec_PROGRAMS = sshg-blocker

sshg_blocker_SOURCES = \
	attack.c \
	blocker.c \
	blocklist.c \
	blocklist.h \
	fnv.h \
	hash_32a.c \
	sshguard_blacklist.c \
	sshguard_blacklist.h \
	sshguard_log.h \
	sshguard_options.c \
	sshguard_options.h \
	sshguard_whitelist.c \
	sshguard_whitelist.h
sshg_blocker_LDADD = \
	$(top_srcdir)/src/common/libsandbox.a \
	$(top_srcdir)/src/common/libservice_names.a \
	$(top_srcdir)/src/common/libsimclist.a

LOG_DRIVER = env AM_TAP_AWK='$(AWK)' $(SHELL) \
			 $(top_srcdir)/tap-driver.sh

TESTS = test-sshg-blocker
EXTRA_DIST = $(TESTS)
