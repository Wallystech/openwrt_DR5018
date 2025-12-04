include $(TOPDIR)/rules.mk

PKG_NAME:=mini-web-core
PKG_VERSION:=1
PKG_RELEASE:=1
LOCAL_SRC:=$(TOPDIR)/qca/src/wallys/mini-web-src/mini-web-vue2
include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
  SECTION:=wallys
  CATEGORY:=Wallys
  SUBMENU:=Web Applications
  TITLE:=Wallys mini web core
  DEPENDS:=+oui-rpc-core
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
	$(CP) -rf $(LOCAL_SRC)/* $(PKG_BUILD_DIR)/
endef

define Build/Compile
		npm --prefix $(PKG_BUILD_DIR) install && \
		npm --prefix $(PKG_BUILD_DIR) run build;
endef

define Package/$(PKG_NAME)/install
		$(INSTALL_DIR) $(1)/www/mini-web
		$(CP) $(PKG_BUILD_DIR)/dist/* $(1)/www/mini-web
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
