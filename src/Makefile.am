#  Copyright 2005 Adam Jackson.
#
#  Permission is hereby granted, free of charge, to any person obtaining a
#  copy of this software and associated documentation files (the "Software"),
#  to deal in the Software without restriction, including without limitation
#  on the rights to use, copy, modify, merge, publish, distribute, sub
#  license, and/or sell copies of the Software, and to permit persons to whom
#  the Software is furnished to do so, subject to the following conditions:
#
#  The above copyright notice and this permission notice (including the next
#  paragraph) shall be included in all copies or substantial portions of the
#  Software.
#
#  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
#  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
#  FITNESS FOR A PARTICULAR PURPOSE AND NON-INFRINGEMENT.  IN NO EVENT SHALL
#  ADAM JACKSON BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
#  IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
#  CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

# this is obnoxious:
# -module lets us name the module exactly how we want
# -avoid-version prevents gratuitous .0.0.0 version numbers on the end
# _ladir passes a dummy rpath to libtool so the thing will actually link
# TODO: -nostdlib/-Bstatic/-lgcc platform magic, not installing the .a, etc.
AM_CFLAGS = @XORG_CFLAGS@ -mips32r2 -Wall
btsm750_drv_la_LTLIBRARIES = btsm750_drv.la
btsm750_drv_la_LDFLAGS = -module -avoid-version
btsm750_drv_ladir = @moduledir@/drivers

#btsm750confdir=$(sysconfdir)/X11/xorg.conf.d
#dist_btsm750conf_DATA = 20-btsm750.conf 30-screen.conf

btsm750_drv_la_SOURCES = \
         compat-api.h \
         uthash.h \
         arm_asm.S \
         cpuinfo.c \
         cpuinfo.h \
         cpu_backend.c \
         cpu_backend.h \
         fb_copyarea.c \
         fb_copyarea.h \
         backing_store_tuner.c \
         backing_store_tuner.h \
         interfaces.h \
         fbdev.c \
         fbdev_priv.h \
         sunxi_disp.c \
         sunxi_disp.h \
         sunxi_x_g2d.c \
         sunxi_x_g2d.h \
         sunxi_disp_hwcursor.c \
         sunxi_disp_hwcursor.h \
         sunxi_video.c \
         sunxi_video.h \
         sunxi_disp_ioctl.h \
         g2d_driver.h \
         sm750_ioctl.h \
				 sm750_output.c \
				 sm750_output.h

if HAVE_LIBUMP
btsm750_drv_la_SOURCES += \
         sunxi_mali_ump_dri2.c \
         sunxi_mali_ump_dri2.h
endif
