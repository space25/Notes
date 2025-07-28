## Setup:
1.  Install:
  ```
  apt install qemu-kvm
  ```
2.  QEMU tools:
  ```
  sudo apt install -y qemu-kvm bridge-utils libvirt-daemon virt-manager \
  libvirt-clients libvirt-daemon-system
  ```
  ```
  sudo adduser $USER libvirt
  ```
3.  Create disk:
  ```
  qemu-img create -f qcow2 disk1.qcow2 50G
  ```
4.  Create a basic QEMU guest using KVM:
  ```
  sudo qemu-system-x86_64 \
    -enable-kvm \
    -cpu host \
    -smp 4 \
    -vga virtio -display sdl,gl=on \
    -m 8G \
    -k en-us \
    -usbdevice tablet \
    -drive file=disk1.qcow2,if=virtio \
    -cdrom ubuntu-22.04.4-desktop-amd64.iso \
    -monitor stdio \
    -device qemu-xhci,id=xhci \
    -device usb-host,bus=xhci.0,vendorid=0x058f,productid=0x6387 \
    -boot menu=on \
    -nic user,hostfwd=::2222-:22,hostfwd=::8080-:80
  ```


## Links:
* [Notes and Snippets for Virtualization with QEMU and KVM on LinkedIn Learning](https://github.com/LinkedInLearning/virtualization-with-kvm-and-qemu-2487226/blob/main/Notes.md)
* [QEMU: A proper guide!](https://www.youtube.com/watch?v=AAfFewePE7c&t=488s)
* [Clipboard copy and paste in QEMU](https://www.youtube.com/watch?v=DcgF7-OHRTo)
* [How To Emulate Firmware With QEMU - Hardware Hacking Tutorial](https://www.youtube.com/watch?v=3yP3QOT-h98)
