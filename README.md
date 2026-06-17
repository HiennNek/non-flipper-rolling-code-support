# 🔑 Rolling code support for "DIY Flipper" & Kiisu

> Enable rolling code support on Kiisu, DIY Flipper Zero, and other unofficial devices -
> **no coding skills or firmware compilation required.**
> 
> ✅ Compatible with all Flipper Zero firmware forks - Official, Unleashed, Momentum, RogueMaster, and more.

---

## 📋 Table of Contents

- [Installation](#-installation)
- [Background](#-background)
- [Missing Keys](#-missing-keys)
- [Contributing](#-contributing)

---

## ⚡ Installation

**Please read the instructions carefully before proceeding!**

1. Download [`keeloq_mfcodes_user`](https://github.com/HiennNek/non-flipper-rolling-code-support/blob/main/keeloq_mfcodes_user)
2. Open **qFlipper**, **Flipper Lab**, or mount your SD card directly
3. Place the file at: `SD Card/subghz/assets/`
4. Done - no reboot required!

> [!IMPORTANT]
> **Note for Kiisu users:**
>
> [`keeloq_mfcodes_user`](https://github.com/HiennNek/non-flipper-rolling-code-support/blob/main/keeloq_mfcodes_user) does **not** add support for Alutech, Came Atomo, and Nice Flor S, as those keystores are stored as RAW files and require separate handling.
>
> To enable them, download the following files from the Kiisu firmware and place them in `SD Card/subghz/assets/`, replacing the existing ones:
> - [alutech_at_4n](https://github.com/kiisu-io/kiisu-firmware/blob/kiisudev/applications/main/subghz/resources/subghz/assets/alutech_at_4n)
> - [came_atomo](https://github.com/kiisu-io/kiisu-firmware/blob/kiisudev/applications/main/subghz/resources/subghz/assets/came_atomo)
> - [nice_flor_s](https://github.com/kiisu-io/kiisu-firmware/blob/kiisudev/applications/main/subghz/resources/subghz/assets/nice_flor_s)
>
> **(Optional)** For best compatibility, also replace `keeloq_mfcodes` in the same folder with the Kiisu-encrypted version: [keeloq_mfcodes](https://github.com/kiisu-io/kiisu-firmware/blob/kiisudev/applications/main/subghz/resources/subghz/assets/keeloq_mfcodes)

---

## 📖 Background

Flipper Zero firmware(s) is open source, which means it's possible to run it on custom hardware - whether that's a DIY build around an STM microcontroller or a third-party device like the Kiisu, a more affordable alternative to the official Flipper Zero.

There's a catch, though: rolling code support depends on **manufacturer keys** that are encrypted and stored in **slot 1 of the official Flipper Zero's secure enclave**. These keys are tied to official hardware, meaning unofficial devices have no way to access or decrypt them.

This is fundamentally different from U2F, where you can supply your own key and handle the certificate side yourself (newer Kiisu batches even support U2F across all Flipper firmware forks). Rolling code requires the **original, unencrypted manufacturer keys** - there's no workaround.

That's exactly why this repository exists: to give anyone running Flipper firmware(s) on unofficial hardware the ability to interact with rolling code devices, just like a genuine Flipper Zero. And since the fix is simply a drop-in asset file, it works across **all firmware forks** - Official, Unleashed, Momentum, RogueMaster, and any other fork that follows the standard Sub-GHz asset structure.

> [!IMPORTANT]
> All keys in this repository are sourced from **publicly available leaked data**. They were not extracted from a real Flipper Zero or Kiisu firmware fork. This is purely a curated collection of publicly known keys.

---

## ❓ Missing Keys

This file covers most manufacturer keys found across Flipper firmware forks, but not all. The following keys are currently missing:

| Manufacturer Key   | Source Firmware(s) |
|--------------------|--------------------|
| Clemsa_Mutancode   | Unleashed          |
| Wisniowski         | Unleashed          |
| ATA_PTX4           | Unleashed          |
| Fadini             | Unleashed          |
| Seav               | Unleashed          |
| Pujol              | Unleashed          |
| Pujol_Vario        | Unleashed          |
| Erreka             | Unleashed          |
| Mc_Garcia          | Unleashed          |
| Doormatic          | Unleashed          |
| Elvox              | Unleashed          |
| Verex              | Unleashed          |
| ET_Blue            | Unleashed          |
| ET_Blue_Mix        | Unleashed          |

---

## 🤝 Contributing

Contributions are welcome! If you have a missing key, feel free to open a pull request. Please include the manufacturer name and the firmware(s) it was sourced from.
