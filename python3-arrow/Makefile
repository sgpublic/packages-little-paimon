#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=arrow
PKG_VERSION:=1.2.2
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=05caf1fd3d9a11a1135b2b6f09887421153b94558e5ef4d090b567b47173ac2b

PKG_MAINTAINER:=arrow-py
PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-$(PKG_NAME)
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=python3-$(PKG_NAME)
  URL:=https://github.com/arrow-py/arrow
	DEPENDS:=+python3 +python3-dateutil
endef

define Package/python3-$(PKG_NAME)/description
  Arrow is a Python library that offers a sensible and human-friendly
	approach to creating, manipulating, formatting and converting dates,
	times and timestamps. It implements and updates the datetime type,
	plugging gaps in functionality and providing an intelligent module API
	that supports many common creation scenarios. Simply put, it helps you
	work with dates and times with fewer imports and a lot less code.
endef

$(eval $(call Py3Package,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)-src))
