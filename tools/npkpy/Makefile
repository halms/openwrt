#
# Copyright (C) 2023 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk

PKG_NAME:=npkpy
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/john-tho/npkpy.git
PKG_SOURCE_DATE:=2023-01-22
PKG_SOURCE_VERSION:=771dddc5aaaff95a9b4160d6867152cfa1a9255f
PKG_MIRROR_HASH:=430375e34117f39cd557025ca7ea84cfad9ac209ee911f3c41f2a5c22f77b886

include $(INCLUDE_DIR)/host-build.mk

define Host/Compile
endef

define Host/Install
	mkdir -p $(STAGING_DIR_HOST)/share/npkpy
	$(CP) $(HOST_BUILD_DIR)/npkpy $(STAGING_DIR_HOST)/share/npkpy/
	$(CP) $(HOST_BUILD_DIR)/tools/demo_pack_kernel/poc_pack_kernel.py $(STAGING_DIR_HOST)/share/npkpy/pack_npk_kernel.py
endef

define Host/Clean
	rm -rf $(STAGING_DIR_HOST)/share/npkpy
endef

$(eval $(call HostBuild))
