## Setup:
1. Install:
  ```
  apt install qemu-kvm qemu
  ```
2. [Optional] QEMU tools:
  ```
  sudo apt install libvirt-daemon-system libvirt-clients\
  virt-manager
  ```
2. Create disk:
  ```
  qemu-img create -f qcow2 disk1.qcow2 50G
  ```
3. Create a basic QEMU guest using KVM:
  ```
  qemu-system-x86_64 \
    -enable-kvm \
    -cpu host \
    -smp 4 \
    -vga virtio -display sdl,gl=on \
    -m 8G \
    -k en-us \
    -usbdevice tablet \
    -drive file=disk1.qcow2,if=virtio \
    -cdrom ubuntu-22.04.4-desktop-amd64.iso \
    -boot menu=on
  ```


## Links:
* [Notes and Snippets for Virtualization with QEMU and KVM on LinkedIn Learning](https://github.com/LinkedInLearning/virtualization-with-kvm-and-qemu-2487226/blob/main/Notes.md)
* [QEMU: A proper guide!](https://www.youtube.com/watch?v=AAfFewePE7c&t=488s)
* [Clipboard copy and paste in QEMU](https://www.youtube.com/watch?v=DcgF7-OHRTo)
