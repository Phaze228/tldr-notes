# Qemu Patch
- CPU Host, threads, and better graphics acceleration, bootable menu
`qemu-system-i386 -hda $image_path -cdrom $iso -boot menu=on -cpu host -smp 2 -vga virtio -display sdl,gl=on`
