obj-m := i2s_master_loader.o
KDIR := /lib/modules/$(shell uname -r)/build
PWD := $(shell pwd)

all:
	# copy the source file to avoid maintaining multiple copies inside the Makefile folders
	# We tried to use KBUILD_OUTPUT but the module was not compiling
	cp ../src/loader.c i2s_master_loader.c
	$(MAKE) -C $(KDIR) M=$(PWD) modules
	rm i2s_master_loader.c

clean:
	$(MAKE) -C $(KDIR) M=$(PWD) clean

