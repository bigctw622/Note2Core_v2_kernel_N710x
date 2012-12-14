#
# linux/arch/arm/vfp/Makefile
#
# Copyright (C) 2001 ARM Limited
#

# ccflags-y := -DDEBUG
# asflags-y := -DDEBUG

# switch to vfp hard float libraries
# gcc documentation requires -funsafe-math-optimisations to be specified on the primary makefile KBUILD_CFLAGS parameters list
# to be effective
KBUILD_AFLAGS  :=$(KBUILD_AFLAGS:-mhard-float=-Wa,-mfpu=vfpv3)
LDFLAGS		+=--no-warn-mismatch

obj-y			+= vfp.o

vfp-$(CONFIG_VFP)	+= vfpmodule.o entry.o vfphw.o vfpsingle.o vfpdouble.o
