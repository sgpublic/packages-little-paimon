#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME_BASE:=colorama
PKG_NAME:=$(PKG_NAME_BASE)-0.4.5
PKG_VERSION:=0.4.5
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME_BASE)
PKG_HASH:=e6c6b4334fc50988a639d9b98aa429a0b57da6e17b9a44f0451f930b6967b7a4

PKG_MAINTAINER:=tartley
PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-$(PKG_NAME)
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=python3-$(PKG_NAME_BASE)-0.4.5
  URL:=https://github.com/tartley/colorama
  DEPENDS:=+python3
endef

define Package/python3-$(PKG_NAME)/description
Makes ANSI escape character sequences
(for producing colored terminal text and cursor positioning) work under MS Windows.
endef

$(eval $(call Py3Package,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)-src))
