#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=httpx
PKG_VERSION:=0.23.0
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=f28eac771ec9eb4866d3fb4ab65abd42d38c424739e80c08d8d20570de60b0ef

PKG_MAINTAINER:=encode
PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=LICENSE.rst

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-$(PKG_NAME)
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=python3-$(PKG_NAME)
  URL:=https://github.com/encode/httpx
	DEPENDS:=+python3 +python3-certifi +python3-httpcore +python3-rfc3986 +python3-sniffio
endef

define Package/python3-$(PKG_NAME)/description
  HTTPX is a fully featured HTTP client library for Python 3. It includes an
	integrated command line client, has support for both HTTP/1.1 and HTTP/2, and
	provides both sync and async APIs.
endef

$(eval $(call Py3Package,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)-src))
