#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=chevron
PKG_VERSION:=0.14.0
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=87613aafdf6d77b6a90ff073165a61ae5086e21ad49057aa0e53681601800ebf

PKG_MAINTAINER:=noahmorrison
PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE.APACHE2

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-$(PKG_NAME)
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=python3-$(PKG_NAME)
  URL:=https://github.com/noahmorrison/chevron
	DEPENDS:=+python3
endef

define Package/python3-$(PKG_NAME)/description
A python implementation of the mustache templating language.
endef

$(eval $(call Py3Package,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)-src))
