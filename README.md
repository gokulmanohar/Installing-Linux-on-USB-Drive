# Installing-Linux-on-USB-Drive
Article showing how you can install linux (pretty much any distro) on a USB pendrive.

# How to Install Linux OS on USB Drive

---

If you are running *low on hard-disk space* or you want a separate installation of Linux OS without making changes to your primary partition or you don’t want to dual boot, you can try installing Linux (Pretty much any distro will work).  

---

## Requirements

1. One USB pendrive (4 GB or above). This will become our bootable pendrive.
2. One Main USB pendrive where we are going to install Linux. Preferably USB 3.1 with atleast 64 GB of space.
3. One computer that have at least 4 GB of RAM.
4. Internet connection (optional).

## Steps

1. Make USB bootable pendrive with tools such as Rufus or BalenaEtcher etc.
<a href="http://imgbox.com/eKYuMxcH" target="_blank"><img src="https://images2.imgbox.com/58/71/eKYuMxcH_o.png" alt="image host"/></a>

2. Boot into the linux distro using the bootable pendrive. (If you have an option for booting with proprietary Nvidia drivers skip it,
boot into normal mode)  
<a href="http://imgbox.com/7kGL0z0R" target="_blank"><img src="https://images2.imgbox.com/79/02/7kGL0z0R_o.png" alt="image host"/></a>

3. Now plug in your main USB to the system.

4. Click on the install icon.
<a href="http://imgbox.com/Nqa2C8xh" target="_blank"><img src="https://images2.imgbox.com/1f/4e/Nqa2C8xh_o.png" alt="image host"/></a>

5. Go through the process till you see an option to select the installation type. Select `Something else` from here.
<a href="http://imgbox.com/YIcgHJYt" target="_blank"><img src="https://images2.imgbox.com/2d/0e/YIcgHJYt_o.jpg" alt="image host"/></a>

6. This is the most important step in this tutorial. Here you need to find out where your Main USB drive is mounted. Mine was in `/dev/sdb`.
(You can verify it by checking the size of the USB or by going to GParted).

7. Now double click on the option with the size labelled to it. Now mine was `/dev/sdb1`. Format it to **ext4** and choose the mount point to **/**.
<a href="http://imgbox.com/DJfs3zvX" target="_blank"><img src="https://images2.imgbox.com/ff/31/DJfs3zvX_o.png" alt="image host"/></a>

8. Now again an important step. Select the 'Device for bootloader installation' as your USB drive. In  my case `/dev/sdb`.

9. Now hit 'Install Now'. Go through the process.

10. It will take some time (about 20-30 minutes) for the installation to complete.

11. Once finished, it will ask to reboot the system. Reboot and you have sucessfully installed Linux OS on your pendrive.

---

## Notes

* Use a 3.0 or 3.1 USB as the main USB Drive where you install the OS. This makes world of a difference in loading time and overall performance.
* Inorder to boot into the bootable pendrive, you must enable the 'Boot from USB' option from BIOS. [How to Boot from a USB Drive](https://www.lifewire.com/how-to-boot-from-a-usb-device-2626091)
* Don't choose the option of Installing for Nvidia drivers from the boot screen. As it worsens the overall experience. The delay of communication from
the USB port to the graphic driver is very high.
* Use your internet connection to download necessary updates and optional files while installing if you want to have a full fledged OS after installation.
* Don't expect your system to perform as a beast. Installing OS on USB has it's own drawbacks.
* If you want you can make any computer to be your private system with this USB. Use 32 bit Linux OS to make it compatible with any available PC.

