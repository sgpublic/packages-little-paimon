#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=cookiecutter
PKG_VERSION:=1.7.3
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=f3982be8d9c53dac1261864013fdec7f83afd2e42ede6f6dd069c5e149c540d5

PKG_MAINTAINER:=cookiecutter
PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE.rst

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-$(PKG_NAME)
  SECTION:=lang
  CATEGORY:=Language
  SUBMENU:=Python
  TITLE:=python3-$(PKG_NAME)
  URL:=https://github.com/cookiecutter/cookiecutter
	DEPENDS:=+python3 +python3-binaryornot +python3-click +python3-jinja2 \
	 +python3-jinja2-time +python3-poyo +python3-slugify +python3-requests \
	 +python3-six
endef

define Package/python3-$(PKG_NAME)/description
  A command-line utility that creates projects from cookiecutters (project templates), e.g.
	creating a Python package project from a Python package project template.
endef

$(eval $(call Py3Package,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)-src))
