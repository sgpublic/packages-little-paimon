#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=prompt-toolkit
PKG_VERSION:=3.0.30
PKG_RELEASE:=1

PYPI_NAME:=prompt_toolkit
PKG_HASH:=859b283c50bde45f5f97829f77a4674d1c1fcd88539364f1b28a37805cfd89c0

PKG_MAINTAINER:=prompt-toolkit
PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-$(PKG_NAME)
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=python3-$(PKG_NAME)
  URL:=https://github.com/prompt-toolkit/python-prompt-toolkit
	DEPENDS:=+python3 +python3-wcwidth
endef

define Package/python3-$(PKG_NAME)/description
prompt_toolkit is a library for building powerful interactive command line
applications in Python.
endef

$(eval $(call Py3Package,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)-src))
