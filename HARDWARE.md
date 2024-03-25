# Hardware

- Motherboard: [Supermicro H12SSL-I](https://www.supermicro.com/en/products/motherboard/h12ssl-i), BIOS 2.7.
- CPU: AMD [EPYC 7543](https://www.amd.com/en/products/cpu/amd-epyc-7543) 32 cores.
- GPU: 2x NVIDIA [RTX A5000](https://www.nvidia.com/en-us/design-visualization/rtx-a5000/).
- RAM: 512GB DDR4.
  - 8x Samsung DIMM DDR4 3200 MHz ([M393A8G40AB2-CWE](https://semiconductor.samsung.com/dram/module/rdimm/m393a8g40ab2-cwe/)).
- Hard Drives:
  - 3x Seagate [ST4000NM000B-2TF100](https://www.seagate.com/products/enterprise-drives/exos-e/7e10/) 4TB
  - 1x Samsung [SSD 990 PRO](https://semiconductor.samsung.com/consumer-storage/internal-ssd/990-pro/) 1TB.

## Inxi

```bash
root@enterprise:~# inxi -Fc0
System:
  Host: enterprise Kernel: 6.6.5-060605-generic x86_64 bits: 64 Console: pty pts/3
    Distro: Ubuntu 22.04.4 LTS (Jammy Jellyfish)
Machine:
  Type: Server System: Supermicro product: Super Server v: 0123456789 serial: 0123456789
  Mobo: Supermicro model: H12SSL-I v: 1.02 serial: WM235S607346 UEFI: American Megatrends
    v: 2.7 date: 10/25/2023
CPU:
  Info: 32-core model: AMD EPYC 7543 bits: 64 type: MT MCP cache: L2: 16 MiB
  Speed (MHz): avg: 1620 min/max: 1500/3738 cores: 1: 1500 2: 1500 3: 1500 4: 2800 5: 1500
    6: 1500 7: 1500 8: 1500 9: 1500 10: 1500 11: 1500 12: 1500 13: 1500 14: 1500 15: 1500 16: 1500
    17: 1500 18: 1500 19: 1500 20: 1500 21: 1500 22: 1500 23: 1500 24: 1500 25: 1500 26: 1500
    27: 1500 28: 1500 29: 1500 30: 1500 31: 1500 32: 1500 33: 1500 34: 1500 35: 1500 36: 1500
    37: 2100 38: 1500 39: 2800 40: 1500 41: 1500 42: 1500 43: 1500 44: 1500 45: 1500 46: 1500
    47: 1500 48: 2800 49: 1500 50: 1500 51: 1500 52: 1500 53: 1500 54: 2100 55: 1500 56: 1500
    57: 2800 58: 2800 59: 1500 60: 1500 61: 1500 62: 1500 63: 1500 64: 1500
Graphics:
  Device-1: ASPEED Graphics Family driver: ast v: kernel
  Device-2: NVIDIA GA102GL [RTX A5000] driver: nvidia v: 550.54.15
  Device-3: NVIDIA GA102GL [RTX A5000] driver: nvidia v: 550.54.15
  Display: server: X.org v: 1.21.1.4 driver: gpu: ast note:  X driver n/a tty: 180x50
Audio:
  Device-1: NVIDIA GA102 High Definition Audio driver: snd_hda_intel
  Device-2: NVIDIA GA102 High Definition Audio driver: snd_hda_intel
  Sound Server-1: ALSA v: k6.6.5-060605-generic running: yes
Network:
  Device-1: Broadcom NetXtreme BCM5720 Gigabit Ethernet PCIe driver: tg3
  IF: eno1 state: up speed: 1000 Mbps duplex: full mac: 3c:ec:ef:e2:cc:1a
  Device-2: Broadcom NetXtreme BCM5720 Gigabit Ethernet PCIe driver: tg3
  IF: eno2 state: down mac: 3c:ec:ef:e2:cc:1b
  IF-ID-1: enxbe3af2b6059f state: down mac: be:3a:f2:b6:05:9f
  IF-ID-2: tailscale0 state: unknown speed: -1 duplex: full mac: N/A
Bluetooth:
  Device-1: Insyde RNDIS/Ethernet Gadget type: USB driver: rndis_host
RAID:
  Device-1: md0 type: mdraid level: raid-5 status: active size: 7.28 TiB report: 3/3 UUU
  Components: Online: 0: sda 1: sdb 3: sdc
Drives:
  Local Storage: total: raw: 11.83 TiB usable: 8.19 TiB used: 28.32 GiB (0.3%)
  ID-1: /dev/nvme0n1 vendor: Samsung model: SSD 990 PRO 1TB size: 931.51 GiB
  ID-2: /dev/sda vendor: Seagate model: ST4000NM000B-2TF100 size: 3.64 TiB
  ID-3: /dev/sdb vendor: Seagate model: ST4000NM000B-2TF100 size: 3.64 TiB
  ID-4: /dev/sdc vendor: Seagate model: ST4000NM000B-2TF100 size: 3.64 TiB
Partition:
  ID-1: / size: 914.78 GiB used: 22.44 GiB (2.5%) fs: ext4 dev: /dev/nvme0n1p2
  ID-2: /boot/efi size: 1.05 GiB used: 6.1 MiB (0.6%) fs: vfat dev: /dev/nvme0n1p1
  ID-3: /home size: 7.22 TiB used: 5.87 GiB (0.1%) fs: ext4 dev: /dev/md0
Swap:
  ID-1: swap-1 type: file size: 8 GiB used: 0 KiB (0.0%) file: /swap.img
Info:
  Processes: 712 Uptime: 3d 21h 29m Memory: 503.54 GiB used: 5.32 GiB (1.1%) Init: systemd
  runlevel: 3 Shell: Bash inxi: 3.3.13
```
