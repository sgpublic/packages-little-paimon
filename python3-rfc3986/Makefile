#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=rfc3986
PKG_VERSION:=1.5.0
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=270aaf10d87d0d4e095063c65bf3ddbc6ee3d0b226328ce21e036f946e421835

PKG_MAINTAINER:=python-hyper
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
  URL:=https://github.com/python-hyper/rfc3986/
	DEPENDS:=+python3
endef

define Package/python3-$(PKG_NAME)/description
A Python implementation of RFC 3986 including validation and authority parsing.
endef

$(eval $(call Py3Package,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)-src))
