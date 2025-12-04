include $(TOPDIR)/rules.mk

PKG_NAME:=libbat-lua
PKG_VERSION:=1
PKG_RELEASE:=1
LOCAL_SRC:=$(TOPDIR)/qca/src/wallys/libbat-lua/src
include $(INCLUDE_DIR)/package.mk

TARGET_CFLAGS += $(FPIC) -I$(STAGING_DIR)/usr/include/lua5.3
TARGET_LDFLAGS += -lm


define Package/$(PKG_NAME)
  SECTION:=wallys
  CATEGORY:=Wallys
  SUBMENU:=Web Applications
  DEPENDS:=+libnl-tiny +libc +librt +liblua5.3
  TITLE:=Wallys batlib lua
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
	$(CP) -rf $(LOCAL_SRC)/* $(PKG_BUILD_DIR)/
endef

define Build/Compile
	$(TARGET_CC) $(TARGET_CFLAGS) $(TARGET_LDFLAGS) -shared \
		-o $(PKG_BUILD_DIR)/batlib.so
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/local/lib/lua/5.3
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/batlib.so $(1)/usr/local/lib/lua/5.3
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
