#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=nonebot2
PKG_VERSION:=2.0.0b4
PKG_RELEASE:=1

PYPI_NAME:=$(PKG_NAME)
PKG_HASH:=fe57242138b3ab7019770566c23f7b39c53e0159b81ec7bd5b34cf6b1ff9eb13

PKG_MAINTAINER:=nonebot
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
  URL:=https://github.com/nonebot/nonebot2
	DEPENDS:=+python3 +python3-fastapi +python3-loguru +python3-pydantic \
	  +python3-pygtrie +python3-tomlkit +python3-typing-extensions \
		+python3-uvicorn +python3-yarl
endef

define Package/python3-$(PKG_NAME)/description
NoneBot2 is a modern, cross-platform, and extensible Python chatbot framework.
It is based on Python's type annotations and asynchronous features, and can
provide convenient and flexible support for your needs.
endef

$(eval $(call Py3Package,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)-src))
