#
# Copyright (C) 2019-2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=littlepaimon-utils
PKG_VERSION:=1.0.2
PKG_RELEASE:=1

PYPI_NAME:=littlepaimon_utils
PKG_HASH:=c072b3560a1506fd76141e2c07ba2eefed9640f6ab4ff6739aed06c1582259ec

PKG_MAINTAINER:=CMHopeSunshine
PKG_LICENSE:=AGPL
PKG_LICENSE_FILES:=LICENSE

include $(TOPDIR)/feeds/packages/lang/python/pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk

define Package/python3-$(PKG_NAME)
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=python3-$(PKG_NAME)
  URL:=https://pypi.org/project/littlepaimon-utils
	DEPENDS:=+python3 +python3-httpx +python3-pillow
endef

define Package/python3-$(PKG_NAME)/description
The author of this package has not provided a project description
endef

$(eval $(call Py3Package,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)))
$(eval $(call BuildPackage,python3-$(PKG_NAME)-src))
