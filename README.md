# 🔑 Rolling code support for "DIY Flipper"

> Add rolling code support on DIY Flipper Zero & other unofficial devices -
> **no coding skills or firmware compilation required.**
> 
> ✅ Compatible with all Flipper Zero firmware forks - Official, Unleashed, Momentum, RogueMaster, and more.

> [!IMPORTANT]
> **For Kiisu v4b/v4br users**: Please use my Momentum/Unleashed fork: [Kiisu-MNTM](https://github.com/HiennNek/kiisu-mntm) / [Kiisu-UNLSHD](https://github.com/HiennNek/kiisu-unlshd). They are up to date with upstream FWs, have rolling codes & U2F support, and Kiisu apps + Kiisu assets + Kiisu tweaks from Kiisu FW.

---

## 📋 Table of Contents

- [Installation](#-installation)
- [Background](#-background)
- [Missing Keys](#-missing-keys)
- [Contributing](#-contributing)

---

## ⚡ Installation

**Please read the instructions carefully before proceeding!**

**Make sure you're using the latest firmware!**

1. Download [`keeloq_mfcodes_user`](https://github.com/HiennNek/non-flipper-rolling-code-support/blob/main/keeloq_mfcodes_user)
2. Open **qFlipper**, **Flipper Lab**, or mount your SD card directly
3. Place the file at: `SD Card/subghz/assets/`
4. Done - no reboot required!

> [!IMPORTANT]
> Alutech AT-4N and Nice Flor-S are not supported. Those two protocols/manufacturers used RAW keystore and can't be stored as unencrypted.

---

## 📖 Background

Flipper Zero firmware(s) are open source, which means it's possible to run them on custom hardware - whether that's a DIY build around an STM microcontroller or a third-party device like the Kiisu, a more affordable alternative to the official Flipper Zero.

There's a catch, though: rolling code support depends on **manufacturer keys** that are encrypted and stored in **slot 1 of the official Flipper Zero's secure enclave**. These keys are tied to official hardware, meaning unofficial devices have no way to access or decrypt them.

This is fundamentally different from U2F, where you can supply your own key and handle the certificate side yourself. Rolling code requires the **original, unencrypted manufacturer keys** - there's no workaround.

That's exactly why this repository exists: to give anyone running Flipper firmware(s) on unofficial hardware the ability to interact with rolling code devices, just like a genuine Flipper Zero. And since the fix is simply a drop-in asset file, it works across **all firmware forks** - Official, Unleashed, Momentum, RogueMaster, and any other fork that follows the standard Sub-GHz asset structure.

> [!IMPORTANT]
> All keys in this repository are sourced from **publicly available leaked data**. They were not extracted from a real Flipper Zero or Kiisu firmware fork. This is purely a curated collection of publicly known keys.

---

## ❓ Missing Keys

This file covers most manufacturer keys found across Flipper firmware forks, but not all. The following keys are currently missing:

|  Manufacturer Key  |
|--------------------|
| Clemsa Mutancode   | 
| Wisniowski         | 
| ATA PTX4           | 
| Fadini             | 
| Seav               | 
| Pujol              | 
| Pujol Vario        | 
| Erreka             | 
| Mc Garcia          | 
| Doormatic          | 
| Elvox              | 
| Verex              | 
| ET Blue            | 
| ET Blue Mix        |
| AERF protocols     |
| JCM1G protocols    |
| Miserere           |

Those missing manufacturer keys came from Unleashed commit [63d49b6](https://github.com/DarkFlippers/unleashed-firmware/commit/63d49b6e48533c8a182f3d0af97c59e629f07706). Keys from older commits are fully added.

---

## 🤝 Contributing

Contributions are welcome! If you have a missing key, feel free to open a pull request. Please include the manufacturer name and the firmware(s) it was sourced from.
