# SPDX-License-Identifier: GPL-3.0-only
#
# Copyright (C) 2021 sgpublic

include $(TOPDIR)/rules.mk

PKG_NAME:=little-paimon
PKG_VERSION:=1.0.1
PKG_RELEASE:=1

PKG_MAINTAINER:=CMHopeSunshine
PKG_LICENSE:=GPL-3.0
PKG_LICENSE_FILE:=LICENSE

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Tencent
  TITLE:=little-paimon
  URL:=https://github.com/CMHopeSunshine/LittlePaimon
	DEPENDS:=+python3-nb-cli +go-cqhttp +git-http +ffmpeg \
	  +python3-littlepaimon-utils +python3-nonebot-adapter-onebot
endef

define Package/$(PKG_NAME)/description
  Genshin Q group robot based on HoshinoBot, NoneBot2 and go-cqhttp
endef

define Build/Compile
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/etc/little-paimon
	$(CP) ./root/etc/little-paimon/. $(1)/etc/little-paimon
	$(INSTALL_DIR) $(1)/etc/nginx
	$(CP) ./root/etc/nginx/* $(1)/etc/nginx
	$(INSTALL_DIR) $(1)/etc/uci-defaults
	$(INSTALL_BIN) ./files/zzz-little-paimon $(1)/etc/uci-defaults/99-little-paimon
	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) ./root/etc/init.d/* $(1)/etc/init.d
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) ./root/usr/bin/* $(1)/usr/bin
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
