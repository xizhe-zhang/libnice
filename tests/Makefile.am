#
# Makefile.am for the Nice Glib ICE library
#
# (C) 2006, 2007 Collabora Ltd.
# (C) 2006, 2007 Nokia Corporation. All rights reserved.
#
# Licensed under MPL 1.1/LGPL 2.1. See file COPYING.

include $(top_srcdir)/common.mk

AM_CFLAGS = \
	$(ERROR_CFLAGS) \
	$(GLIB_CFLAGS) \
	-I $(top_srcdir)/agent \
	-I $(top_srcdir)/random \
	-I $(top_srcdir)/socket \
	-I $(top_srcdir)/stun

COMMON_LDADD = $(top_srcdir)/agent/libagent.la $(top_srcdir)/socket/libsocket.la $(GLIB_LIBS)

check_PROGRAMS = \
	test-bsd \
	test \
	test-address \
	test-add-remove-stream \
	test-priority \
	test-mainloop \
	test-fullmode \
	test-restart \
	test-fallback \
	test-thread \
	test-dribble

dist_check_SCRIPTS = \
	check-test-fullmode-with-stun.sh

TESTS = $(check_PROGRAMS) $(dist_check_SCRIPTS)

test_bsd_LDADD = $(COMMON_LDADD)

test_LDADD = $(COMMON_LDADD)

test_thread_LDADD = $(COMMON_LDADD)

test_address_LDADD = $(COMMON_LDADD)

test_add_remove_stream_LDADD = $(COMMON_LDADD)

test_priority_LDADD = $(COMMON_LDADD)

test_mainloop_LDADD = $(COMMON_LDADD)

test_fullmode_LDADD = $(COMMON_LDADD)

test_restart_LDADD = $(COMMON_LDADD)

test_fallback_LDADD = $(COMMON_LDADD)

test_thread_LDADD = $(COMMON_LDADD)

test_dribble_LDADD = $(COMMON_LDADD)

all-local:
	chmod a+x $(srcdir)/check-test-fullmode-with-stun.sh