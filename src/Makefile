# License: GPL v2 or later
# Copyright Red Hat Inc. 2001 - 2008

PKGNAME=system-config-users-docs

SCM_REMOTEREPO_RE = ^ssh://(.*@)?git.fedorahosted.org/git/$(PKGNAME).git$
UPLOAD_URL = ssh://fedorahosted.org/$(PKGNAME)

PREFIX=/usr
DATADIR=${PREFIX}/share

MAKEFILE        := $(lastword $(MAKEFILE_LIST))
TOPDIR          := $(abspath $(dir $(abspath $(MAKEFILE))))
DOC_MODULE      = system-config-users
DOC_ABS_SRCDIR  = $(TOPDIR)/doc
DOC_FIGURES_DIR = images
DOC_FIGURES     = system-config-users-group-new.png system-config-users-group-properties-group-data.png system-config-users.png system-config-users-user-new.png system-config-users-user-properties-user-data.png
DOC_ENTITIES    = distro-specifics.ent system-config-users-distro-specifics.ent system-config-users-abstract.xml system-config-users-content.xml
DOC_LINGUAS_EXCLUDE	=

all:		doc-all
install:	all doc-install
clean:		doc-clean

include doc_rules.mk
include rpmspec_rules.mk
include git_rules.mk
include upload_rules.mk
