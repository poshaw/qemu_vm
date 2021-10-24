# qemu_vm_create

This is a work in progress.

Goal is to launch VMs from the script "vm" that is on the $PATH

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

## Create a new virtual machine named "Linux"
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
│   │   ├── linux.iso -> ${HOME}/Downloads/iso/linux.iso
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
