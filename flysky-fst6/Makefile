#
# Copyright (C) 2016 Martin K. Schröder <mkschreder.uk@gmail.com>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk

ARCH:=arm
BOARD:=flysky-fst6
BOARDNAME:=FlySky FS-T6 Transmitter (ARM)
MAINTAINER:=Martin Schröder <mkschreder.uk@gmail.com>
CPU_TYPE:=cortex-m3

# fs-t6 board comes with 12mhz external crystal so we need to build all stm32 libraries with the proper HSE_VALUE. 
CFLAGS:=-march=armv7-m -mcpu=cortex-m3 -mthumb -DHSE_VALUE=12000000UL

include $(INCLUDE_DIR)/target.mk

define Target/Description
	Build firmware images for the fs-t6 rc transmitter board
endef

$(eval $(call BuildTarget))
