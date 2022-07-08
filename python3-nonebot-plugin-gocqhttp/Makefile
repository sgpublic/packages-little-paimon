#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=nonebot-plugin-gocqhttp
PKG_VERSION:=0.5.5
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=b6160d44dba6cfd0f47219cfb4bb9c08664fef5c3d776132ccada98c2616f84f

PKG_MAINTAINER:=mnixry
PKG_LICENSE:=AGPL-3.0
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-$(PKG_NAME)
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=python3-$(PKG_NAME)
  URL:=https://github.com/mnixry/nonebot-plugin-gocqhttp
	DEPENDS:=+python3-chevron +python3-httpx +python3-nonebot-adapter-onebot \
	  +python3-nonebot2 +python3-psutil +python3-py-cpuinfo
endef

define Package/python3-$(PKG_NAME)/description
A plugin to run go-cqhttp directly in NoneBot2, without additional download and installation.
endef

$(eval $(call Py3Package,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)-src))
