#
#  Top level makefile for GNUstep Backend
#
#  Copyright (C) 2009-2010 Free Software Foundation, Inc.
#
#  Author: Riccardo Mottola
#
#  This file is part of the Windows UX Theme.
#
#  This library is free software; you can redistribute it and/or
#  modify it under the terms of the GNU Lesser General Public
#  License as published by the Free Software Foundation; either
#  version 2 of the License, or (at your option) any later version.
#
#  This library is distributed in the hope that it will be useful,
#  but WITHOUT ANY WARRANTY; without even the implied warranty of
#  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.	 See the GNU
#  Lesser General Public License for more details.
#
#  You should have received a copy of the GNU Lesser General Public
#  License along with this library; see the file COPYING.LIB.
#  If not, see <http://www.gnu.org/licenses/> or write to the 
#  Free Software Foundation, 51 Franklin Street, Fifth Floor, 
#  Boston, MA 02110-1301, USA.

ifeq ($(GNUSTEP_MAKEFILES),)
 GNUSTEP_MAKEFILES := $(shell gnustep-config --variable=GNUSTEP_MAKEFILES 2>/dev/null)
endif

ifeq ($(GNUSTEP_MAKEFILES),)
  $(error You need to set GNUSTEP_MAKEFILES before compiling!)
endif


include $(GNUSTEP_MAKEFILES)/common.make

PACKAGE_NAME = WinUXTheme
BUNDLE_NAME = WinUXTheme
BUNDLE_EXTENSION = .theme
VERSION = 1

WinUXTheme_INSTALL_DIR=$(GNUSTEP_LIBRARY)/Themes
WinUXTheme_PRINCIPAL_CLASS = WinUXTheme
ADDITIONAL_OBJC_LIBS=-luxtheme  

WinUXTheme_OBJC_FILES = \
		WinUXTheme.m \
		WinNSButton.m \
		WinNSScroller.m \
		WinNSMenu.m \
		WinNSMenuItemCell.m \
		WIN32VSImageRep.m

#
# Resource files
#
WinUXTheme_RESOURCE_FILES = \
Resources/WinTheme.png \
Resources/ThemeImages/common_3DArrowRight.w32vsr \
Resources/ThemeImages/common_Nibble.tif \
Resources/ThemeImages/common_RadioOff.w32vsr \
Resources/ThemeImages/common_RadioOn.w32vsr \
Resources/ThemeImages/common_SliderHoriz.w32vsr \
Resources/ThemeImages/common_SliderVert.w32vsr \
Resources/ThemeImages/common_SwitchOff.w32vsr \
Resources/ThemeImages/common_SwitchOn.w32vsr

-include GNUmakefile.preamble

include $(GNUSTEP_MAKEFILES)/bundle.make

-include GNUmakefile.postamble

