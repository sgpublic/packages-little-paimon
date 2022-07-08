#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=h11
PKG_VERSION:=0.12.0
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=47222cb6067e4a307d535814917cd98fd0a57b6788ce715755fa2b6c28b56042

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
  URL:=https://github.com/python-hyper/h11
	DEPENDS:=+python3
endef

define Package/python3-$(PKG_NAME)/description
This is a little HTTP/1.1 library written from scratch in Python, heavily
inspired by hyper-h2.
endef

$(eval $(call Py3Package,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)-src))
