obj-m :=ioctl.o

KDIR=/lib/modules/$(shell uname -r)/build/

PWD :=$(shell pwd)

default:
	$(MAKE) -C $(KDIR) M=$(PWD) modules
	gcc -o app app.c

install:
	$(MAKE) -C $(KDIR) M=$(PWD) modules_install

clean:
	$(MAKE) -C $(KDIR) M=$(PWD) clean
	rm app
