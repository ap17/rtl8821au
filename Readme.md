rtl8821au
( idVendor=0bda, idProduct=a811 )
driver v5.2.6.2_23547.20170814_COEX20170206-6760

origin : https://github.com/minjae/rtl8821au

Currently (march 2020) used by me on Xunlong Orange OPi H3 and H5 with Linux 5.6, Debian 10. Works great both in access point mode and in infrastructure mode.

This driver must be built in "in-tree" mode.

1.    put driver sources to ".../drivers/net/wireless/realtek/rtl8821au"
2.    into file ".../drivers/net/wireless/realtek/Kconfig" insert line:

source "/drivers/net/wireless/realtek/rtl8821au/Kconfig"

3.    into file ".../drivers/net/wireless/realtek/Makefile" insert line:

obj-$(CONFIG_RTL8821AU) += rtl8821au/

4.    do : make menuconfig -> device drivers-> network device support -> wireless LAN -> select 8821au
5.    do make.
