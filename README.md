# System Information — Sophia's Laptop

Deep research into the hardware and software configuration of this machine.

---

## Machine Identity

| Field | Value |
|-------|-------|
| **Hostname** | SOPHIA |
| **Manufacturer** | Lenovo |
| **Model** | 81X7 (IdeaPad 3 15ITL6) |
| **Type** | x64-based PC |
| **Owner** | sophi.t2011@gmail.com |
| **BIOS** | Lenovo GCCN37WW (11/04/2024) |
| **Original Install** | 10 June 2025 |

---

## Processor

| Field | Value |
|-------|-------|
| **Name** | Intel Core i5-1135G7 |
| **Generation** | 11th Gen (Tiger Lake) |
| **Base Clock** | 2.40 GHz |
| **Max Turbo** | 4.20 GHz |
| **Cores** | 4 physical |
| **Threads** | 8 logical |
| **Architecture** | x86-64 (Intel64 Family 6 Model 140 Stepping 1) |
| **TDP** | 28W (configurable 12-28W) |
| **Process** | Intel 10nm SuperFin |
| **Integrated GPU** | Intel Iris Xe (80 EU) |
| **PCIe Lanes** | 16 (PCIe 4.0) |
| **Cache** | 8 MB L3 SmartCache |

The i5-1135G7 is a mid-range mobile processor from Intel's Tiger Lake family. It features Willow Cove cores on a 10nm SuperFin process. Supports Thunderbolt 4, Wi-Fi 6, and DDR4-3200.

---

## Memory (RAM)

| Slot | Manufacturer | Part Number | Capacity | Speed |
|------|-------------|-------------|----------|-------|
| 1 | Micron Technology | 4ATF51264HZ-3G2J1 | 4 GB | 3200 MHz |
| 2 | Samsung | M471A5244CB0-CWE | 4 GB | 3200 MHz |

| Field | Value |
|-------|-------|
| **Total Installed** | 8 GB |
| **Type** | DDR4 SODIMM |
| **Speed** | 3200 MHz |
| **Dual Channel** | Yes (mixed vendors) |
| **Max Supported** | 20 GB (4 GB soldered + 1 SODIMM slot) |
| **Virtual Memory** | 19,951 MB max |

> **Note**: One 4 GB module is soldered to the motherboard, one is removable. Mixed vendor modules work but may not run in optimal dual-channel mode.

---

## Graphics

| Field | Value |
|-------|-------|
| **Name** | Intel Iris Xe Graphics |
| **Type** | Integrated (iGPU) |
| **Shared Memory** | ~2 GB (from system RAM) |
| **EU Count** | 80 Execution Units |
| **Driver Version** | 32.0.101.7088 |
| **APIs** | DirectX 12.1, OpenGL 4.6, Vulkan 1.2 |

The Iris Xe is Intel's integrated graphics for 11th Gen. No dedicated GPU — all graphics share system memory. Suitable for light gaming, video playback, and productivity. Not ideal for GPU-heavy workloads like video editing or 3D rendering.

---

## Storage

| Drive | Model | Interface | Size | Type |
|-------|-------|-----------|------|------|
| C: (Windows) | NVMe UMIS RPJTJ256MEE1OWX | NVMe (SCSI) | 256 GB | Fixed SSD |
| D: (Memories) | — | — | ~97.7 GB | Fixed partition |

| Partition | Total | Free | % Free |
|-----------|-------|------|--------|
| C: | 149.9 GB | 42.4 GB | 28% |
| D: | 104.9 GB | 17.3 GB | 16% |

> **Note**: The 256 GB SSD is split into C: and D: partitions. D: is a data partition, not a separate physical drive. The UMIS RPJTJ is a budget NVMe SSD — decent speeds but limited endurance.

---

## Battery

| Field | Value |
|-------|-------|
| **Model** | L16M2PB2 |
| **Type** | Lithium-Ion |
| **Status** | Discharging (2) |
| **Design Capacity** | ~45 Wh (typical for this model) |

---

## Network

| Interface | Details |
|-----------|---------|
| **Wi-Fi** | Intel Wireless-AC 9560 |
| **Wi-Fi Standard** | 802.11ac (Wi-Fi 5) |
| **Bluetooth** | 5.0 |
| **Current IP** | 192.168.1.150 |
| **DHCP Server** | 192.168.1.1 |

> **Note**: The Wireless-AC 9560 supports up to 1.73 Gbps theoretical throughput on 5 GHz. Does not support Wi-Fi 6 (802.11ax).

---

## Display

| Field | Value |
|-------|-------|
| **Size** | 15.6 inches |
| **Resolution** | 1920 × 1080 (Full HD) |
| **Panel Type** | TN (typical for this model) |
| **Touch** | No |

---

## Operating System

| Field | Value |
|-------|-------|
| **OS** | Microsoft Windows 11 Home |
| **Build** | 26200.6725 |
| **Version** | 10.0.26200 |
| **Architecture** | 64-bit |
| **Locale** | en-gb (English United Kingdom) |
| **Time Zone** | UTC+00:00 (London) |
| **Hyper-V** | Detected (hypervisor running) |
| **VBS** | Running with DMA Protection |

### Installed Updates
| KB | Description |
|----|-------------|
| KB5122385 | Cumulative Update |
| KB5050575 | Cumulative Update |
| KB5054156 | Security Update |
| KB5065847 | Cumulative Update |
| KB5065789 | Security Update |
| KB5120997 | Servicing Stack |

---

## Software Stack

| Tool | Version |
|------|---------|
| **Node.js** | v24.19.0 |
| **npx** | 12.0.2 |
| **Git** | Available |
| **OpenCode** | Active |
| **PowerShell** | 5.1 |
| **WSL** | 2.7.12 (Ubuntu installing) |

---

## Limitations & Considerations

1. **8 GB RAM** — Only 4 GB is upgradeable (the other 4 GB is soldered). Heavy multitasking will be constrained.
2. **256 GB SSD** — Limited storage. Consider external/cloud storage for large files.
3. **Integrated Graphics Only** — No dedicated GPU. Not suitable for ML training, video editing, or heavy gaming.
4. **Mixed RAM Vendors** — Micron + Samsung modules work but may not run in optimal dual-channel.
5. **Wi-Fi 5 Only** — No Wi-Fi 6 support, but fine for most use cases.
6. **Windows 10/11 Home** — No Hyper-V management tools (though Hyper-V is detected). WSL2 is the primary virtualization path.

---

## Storage Cleanup History

| Source | Space Recovered |
|--------|----------------|
| npm cache | 5.2 GB |
| Temp files | 433 MB |
| ms-playwright | 701 MB |
| Chrome OptGuideOnDeviceModel | 4 GB |
| **Total** | **~10.6 GB** |

---

*Last updated: 1 September 2026*
