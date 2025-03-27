# Epoch || Makefile
# --------------------------------
# Makefile for generating the Epoch Stub.
# This file should be invoked via the build
# script and not manually.
#
# Configuration derived from the work of:
#
# * @bztsrc <https://gitlab.com/bztsrc>
# * @SerpinskiTriangle <https://github.com/SerpinskiTriangle>
#
# With thanks and respect.
#
# Copyright (C) 2021 bzt (bztsrc@gitlab)
#
# Permission is hereby granted, free of charge, to any person
# obtaining a copy of this software and associated documentation
# files (the "Software"), to deal in the Software without
# restriction, including without limitation the rights to use, copy,
# modify, merge, publish, distribute, sublicense, and/or sell copies
# of the Software, and to permit persons to whom the Software is
# furnished to do so, subject to the following conditions:
#
# The above copyright notice and this permission notice shall be
# included in all copies or substantial portions of the Software.
#
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
# EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
# MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
# NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
# HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
# WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
# OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
# DEALINGS IN THE SOFTWARE.
#
# Original Author:  @bztsrc <https://gitlab.com/bztsrc>
# Contributor:      @SerpinskiTriangle <https://github.com/SerpinskiTriangle>
# Author:           @MaxineToTheStars <https://github.com/MaxineToTheStars>
# ----------------------------------------------------------------

# Architecture
ARCH := x86_64

# Output
TARGET := epoch.efi

# Source files
SRCS := $(wildcard src/*.c)

# Compiler flags
CFLAGS := -pedantic -Wall -Wextra -std=gnu99 -g -O0 -I/usr/include/efi -I/usr/include/efi/$(ARCH) -Iinclude/

# Linker flags
LDFLAGS :=

# Static libraries
LIBS :=

# Output directory
# OUTDIR := build

# Use the native GCC on host
USE_GCC := 1

# Master makefile
include uefi/Makefile
