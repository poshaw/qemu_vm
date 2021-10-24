# qemu_vm_create

This is a work in progress.

Goal is to launch VMs from the script "vm"

## expected directory setup
```
HOME
├── .local
│   └── bin
│       └── vm
├── virtual-machines
│   └── template
│       ├── create
│       ├── install
│       └── run
└── XDG_DOWNLOAD_DIR
    └── iso
        └── linux.iso
```

## Create a new virtual machine
```bash
$ vm -c Linux
```

## Directory structure after creation
```
HOME
├── local
│   └── bin
│       └── vm
├── virtual-machines
│   ├── Linux
│   │   ├── create
│   │   ├── disk.cow
│   │   ├── install
│   │   ├── linux.iso -> ${HOME}/XDG_DOWNLOAD_DIR/iso/linux.iso
│   │   ├── run
│   │   └── uefi_vars.fd
│   └── template
│       ├── create
│       ├── install
│       └── run
└── XDG_DOWNLOAD_DIR
    └── iso
        └── linux.iso
```

When launching a virtual machine "vm" should automatically create a bridge network and a new tap device

Create a pull request for 'dev' on GitHub by visiting:
https://github.com/poshaw/qemu_vm_launcher/pull/new/dev
