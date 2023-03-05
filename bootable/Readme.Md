# How to create a Linux bootable USB on Windows using Rufus

- Example using Kali
1. get a USB3+ drive (at least 8GB).
2. get an [ISO file](https://www.kali.org/get-kali/#kali-live)
3. get [**Rufus**](https://rufus.ie/en/)

![Alt text](/bootable/imgsrc/rufus.png?raw=true "Optional Title")
4. Persistence partition can be useful if any data should persist but is not required. make it 20% of the whole size.
5. Use MBR for legacy compatibility, but if you're sure you're only gonna use it on UEFI compatible machines, that's an option too.

# How to re-format a Linux bootable USB on Windows

1. Open `PowerShell`. Run this command to open: `diskpart`
2. In the diskpart terminal, run these commands (supposing your USB drive is the `disk2`):

```shell
list disk
select disk2
clean
create partition primary
active
```

- format

```shell
format fs=Fat32 quick
```

- if it says `"Virtual Disk Service error: The volume size is too big-"`

```shell
format fs=NTFS quick
```
