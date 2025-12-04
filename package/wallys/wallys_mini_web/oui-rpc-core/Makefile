#
# Copyright (C) 2022 Jianhui Zhao <zhaojh329@gmail.com>
#
# This is free software, licensed under the MIT.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=oui-rpc-core
PKG_VERSION:=1
PKG_RELEASE:=1

PKG_MAINTAINER:=Jianhui Zhao <zhaojh329@gmail.com>
PKG_LICENSE:=MIT
LOCAL_SRC:=$(TOPDIR)/qca/src/wallys/mini-web-src/oui
include $(INCLUDE_DIR)/package.mk

define Package/oui-rpc-core
  SECTION:=wallys
  CATEGORY:=Wallys
  SUBMENU:=Web Applications
  TITLE:=Oui rpc core
  DEPENDS:=+liblua +libuci-lua +lua-cjson +lua-eco-md5 +lua-eco-http +lua-eco-ubus +px5g-mbedtls
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
	$(CP) -rf $(LOCAL_SRC)/* $(PKG_BUILD_DIR)/
endef

Build/Compile=

define Package/oui-rpc-core/install
	$(INSTALL_DIR) $(1)/etc/config $(1)/usr/share/oui $(1)/usr/lib/lua/oui \
		$(1)/usr/share/oui/acl $(1)/usr/sbin $(1)/etc/init.d
	$(INSTALL_CONF) ./files/oui.config $(1)/etc/config/oui
	$(INSTALL_BIN) ./files/oui-httpd.init $(1)/etc/init.d/oui-httpd
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/oui-httpd.lua $(1)/usr/sbin/oui-httpd
	mkdir -p $(1)/usr/local/lib/lua/5.3/oui	
	$(CP) $(PKG_BUILD_DIR)/rpc.lua $(1)/usr/local/lib/lua/5.3/oui/
	$(CP) $(PKG_BUILD_DIR)/zoneinfo.lua $(1)/usr/local/lib/lua/5.3/oui/
	$(CP) $(PKG_BUILD_DIR)/zoneinfolist $(1)/usr/local/lib/lua/5.3/oui/
	$(CP) $(PKG_BUILD_DIR)/rpc $(1)/usr/share/oui
	$(CP) $(PKG_BUILD_DIR)/admin.acl $(1)/usr/share/oui/acl/admin.json
endef

$(eval $(call BuildPackage,oui-rpc-core))
