#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=tomlkit
PKG_VERSION:=0.10.2
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=30d54c0b914e595f3d10a87888599eab5321a2a69abc773bbefff51599b72db6

PKG_MAINTAINER:=sdispater
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-$(PKG_NAME)
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=python3-$(PKG_NAME)
  URL:=https://github.com/sdispater/tomlkit
	DEPENDS:=+python3
endef

define Package/python3-$(PKG_NAME)/description
TOML Kit is a 1.0.0-compliant TOML library.
endef

$(eval $(call Py3Package,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)-src))
