#
# Copyright (c) 2009 Wind River Systems, Inc.
# Tom Rix <Tom.Rix at windriver.com>
#
# See file CREDITS for list of people who contributed to this
# project.
#
# This program is free software; you can redistribute it and/or
# modify it under the terms of the GNU General Public License as
# published by the Free Software Foundation; either version 2 of
# the License, or (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 59 Temple Place, Suite 330, Boston,
# MA 02111-1307 USA
#

include $(TOPDIR)/config.mk

LIB 	:= $(obj)libpower.o

COBJS-$(CONFIG_FTPMU010_POWER)	+= ftpmu010.o
COBJS-$(CONFIG_TWL4030_POWER)	+= twl4030.o
COBJS-$(CONFIG_TWL6030_POWER)	+= twl6030.o
COBJS-$(CONFIG_SUNXI_AXP)		+= axp.o

COBJS-$(CONFIG_SUNXI_AXP22)		+= axp22.o
COBJS-$(CONFIG_SUNXI_AXP22)   	+= axp22_supply.o

COBJS-$(CONFIG_SUNXI_AXP20)		+= axp20.o
COBJS-$(CONFIG_SUNXI_AXP20)   	+= axp20_supply.o

COBJS-$(CONFIG_SUNXI_AXP15)     += axp15.o
COBJS-$(CONFIG_SUNXI_AXP15)     += axp15_supply.o

COBJS-$(CONFIG_SUNXI_AXP809)    += axp809.o
COBJS-$(CONFIG_SUNXI_AXP809)    += axp809_supply.o

COBJS-$(CONFIG_SUNXI_AXP806)    += axp806.o
COBJS-$(CONFIG_SUNXI_AXP806)    += axp806_supply.o

COBJS-$(CONFIG_SUNXI_AXP81X)    += axp81X.o
COBJS-$(CONFIG_SUNXI_AXP81X)    += axp81X_supply.o

COBJS-y                         += axp_null.o
COBJS-y                         += axp_supply_null.o

COBJS	:= $(COBJS-y)
SRCS 	:= $(COBJS:.o=.c)
OBJS 	:= $(addprefix $(obj),$(COBJS))

all:	$(LIB)

$(LIB):	$(obj).depend $(OBJS)
	$(call cmd_link_o_target, $(OBJS))


#########################################################################

# defines $(obj).depend target
include $(SRCTREE)/rules.mk

sinclude $(obj).depend

########################################################################
