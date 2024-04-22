# testing vm

## editor-demo

The editor-demo virtual machine is a KDE wayland environment for testing fltk with fcitx5 (input method).

1. download images

run it on zsh.

```zsh
for url (
    "https://github.com/2moe/testing-vm/releases/download/kde/vm-editor-demo_sid_x64.tar.zst.0"{0..2}
) {
    curl -LO $url
}
```

2. concat files

```zsh
command cat vm-editor-demo_sid_x64.tar.zst.0{0..2} > vm.tzst
rm vm-editor-demo_sid_*
```

3. extract tzst

```sh
tar -xvf vm.tzst
unlink vm.tzst
```

4. install qemu & vnc client

```sh
# run apt as root
apt update
apt install qemu-system-x86 tigervnc-viewer
```

5. run

```sh
./run-vnc
```
