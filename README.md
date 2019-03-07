# rockpi-pcie
PCIe config/devicetree for RockPi boards w/ recent linux kernels (>=5.0)

The devicetrees/configs given here are without video/audio/multimedia support.

Intended purpose: headless systems such as routers/servers

* you should check the kernel config yourself
* some security features (e.g. spectre mitiations) have been disabled for performance benchmarks

* device enumeration is different than with the "normal" RockPi 4.4 kernel
  * ttyS0/2 are swapped (ttyS2 is the serial console with kernel 5.0, ttyS0 for kernel 4.4)
  * microSD card is mmc1 instead of mmc0 with kernel 5.0
  * more stuff may be swapped
  * suggested extlinux cmdline append string: *append earlyprintk rw init=/sbin/init root=**insert_uid** rootwait rootfstype=ext4*
  * early boot console stuff is configured in the devicetree file
