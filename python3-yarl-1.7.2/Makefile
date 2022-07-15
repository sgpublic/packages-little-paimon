#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME_BASE:=yarl
PKG_VERSION:=1.7.2
PKG_NAME:=$(PKG_NAME_BASE)-$(PKG_VERSION)
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME_BASE)
PKG_HASH:=45399b46d60c253327a460e99856752009fcee5f5d3c80b2f7c0cae1c38d56dd

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
  TITLE:=Yet another URL library
  URL:=https://github.com/aio-libs/yarl
  DEPENDS:=+python3 +python3-multidict +python3-idna
endef

define Package/python3-$(PKG_NAME)/description
Yet another URL library
endef

$(eval $(call Py3Package,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)-src))
