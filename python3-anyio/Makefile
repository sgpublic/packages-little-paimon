#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=anyio
PKG_VERSION:=3.6.1
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=413adf95f93886e442aea925f3ee43baa5a765a64a0f52c6081894f9992fdd0b

PKG_MAINTAINER:=agronholm
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE.md

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-$(PKG_NAME)
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=python3-$(PKG_NAME)
  URL:=https://github.com/agronholm/anyio
	DEPENDS:=+python3 +python3-idna +python3-sniffio
endef

define Package/python3-$(PKG_NAME)/description
AnyIO is an asynchronous networking and concurrency library that works on top of
either asyncio or trio. It implements trio-like structured concurrency (SC) on
top of asyncio, and works in harmony with the native SC of trio itself.

Applications and libraries written against AnyIO’s API will run unmodified on
either asyncio or trio. AnyIO can also be adopted into a library or application
incrementally – bit by bit, no full refactoring necessary. It will blend in with
native libraries of your chosen backend.
endef

$(eval $(call Py3Package,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)-src))
