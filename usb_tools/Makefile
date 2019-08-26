WIN_DRIVERS_LIBUSB_DIR = C:\Program Files\LibUSB-Win32
WIN_LIBUSB_INCLUDE_DIR = "$(WIN_DRIVERS_LIBUSB_DIR)\include"
WIN_LIBUSB_LIB_DIR = "$(WIN_DRIVERS_LIBUSB_DIR)\lib\gcc"
CC=gcc
CFLAGS=-Wall

linux: usbtool
win: usbtool_win

usbtool:
	$(CC) $(CFLAGS) -o usbtool jz4740_usbtool.c -lusb
usbtool_win:
	$(CC) $(CFLAGS) -o usbtool.exe jz4740_usbtool.c -lusb -I $(WIN_LIBUSB_INCLUDE_DIR) -L $(WIN_LIBUSB_LIB_DIR)

clean-linux:
	rm usbtool
clean-win:
	del usbtool.exe
