This mod replaces the original textures of the game **Indiana Jones and the Infernal Machine** with enhanced versions created using AI upscaling. The goal is to improve the visual quality of the game on modern displays.

## ⚠️ Disclaimer / Important Notice

*   **Rights:** The original assets and the game Indiana Jones and the Infernal Machine are the property of their respective rights holders (Lucasfilm Games / Disney, etc.). I do not claim ownership of the original materials. This mod is a derivative work.
*   **Usage:** This texture pack is provided "as-is" solely for personal, non-commercial use by fans of the game who own a legal copy of Indiana Jones and the Infernal Machine.
*   **Liability:** You use these textures at your own risk. The mod author is not responsible for any potential issues with the game or your computer.
*   **Distribution:** Any commercial use of these enhanced textures is prohibited. When distributing the mod or its derivative versions (if permitted), you must credit the author of the upscale and maintain its non-commercial nature.
*   **Status:** The mod author is not affiliated with the developers or publishers of the game.

---

## Contents

*   [Requirements](#requirements)
*   [Preparation: Unpacking Game Resources](#preparation-unpacking-game-resources)
*   [Mod Installation](#mod-installation)
    *   [Step 1: Installing Textures](#step-1-installing-textures)
    *   [Step 2: Installing OpenJones3D Engine (Required)](#step-2-installing-openjones3d-engine-required)
    *   [Step 3: Patching the Executable (Downgrade)](#step-3-patching-the-executable-downgrade)
    *   [Step 4: Installing dgVoodoo (Recommended)](#step-4-installing-dgvoodoo-recommended)
*   [Tools and Acknowledgements](#tools-and-acknowledgements)
*   [Useful Links](#useful-links)
*   [Optional: Ready-Made Build](#optional-ready-made-build)

---

## Requirements

*   A legal copy of the game **Indiana Jones and the Infernal Machine**.
*   **Unpacked game resources.** See the [Preparation](#preparation-unpacking-game-resources) section below.

---

## Preparation: Unpacking Game Resources

Before installing any mods, including this one, you need to extract ("unpack") the game archives (`.gob` files) in the `Resource` folder.

**There are two main ways to do this:**

1.  **Manual Method:** Follow the detailed instructions on the Jones3D community GitHub:
    [Resource Unpacking Instructions](https://github.com/Jones3D-The-Infernal-Engine/Documentation/blob/main/pre-mod.md)
    *(This method requires using the `gobext` and `cndtool` utilities by Urgon).*

2.  **Using Indy3DModInstaller:** Use the utility by the_kovic, which automates the process. This is generally faster and more convenient.
    *   Download: [Indy3DModInstaller](https://github.com/thekovic/Indy3DModInstaller)
    *   Run the installer and follow its instructions to unpack the resources written in *README* inside the downloaded archive.

**Important:** After unpacking, the original `CD1.gob`, `CD2.gob`, and `JONES3D.gob` files will no longer be used directly by the game. Instead, the game will read files from the folders inside `Resource`.

---

## Mod Installation

### Step 1: Installing Textures

Once the game resources are unpacked:

1.  **Download** the archive containing my AI-upscaled textures from this repository.
2.  **Choose an installation method:**
    *   **Via Indy3DModInstaller:** If you are using this installer, point it to the downloaded texture archive path. It should place the files correctly.
    *   **Manually:** Extract the texture archive. Copy the `mat` folder from the archive into your game's `Resource` folder, agreeing to replace files when prompted.

### Step 2: Installing OpenJones3D Engine (Required)

Launching the game with unpacked resources normally requires developer mode (see Toggle Dev Mod in Indy3DModInstaller), otherwise the game will ask for the CD. To bypass this and get other improvements, it is highly required to install **OpenJones3D** - a modern open-source engine for the game by Urgon.

1.  Go to the [OpenJones3D](https://github.com/smlu/OpenJones3D) repository page.
2.  Download the latest release (usually a zip archive). Or you you can download the latest version via `Releases`.
3.  **Extract the contents of the downloaded archive** directly into your game's `Resource` folder, agreeing to replace files.

### Step 3: Patching the Executable (Downgrade)

OpenJones3D requires the original game executable (`Indy3D.exe`) to be downgraded to version 1.0.

1.  **Find the downgrade files:** Within the files of this repository there should be a folder called downgrade-file containing `.bps` files. Downloading them depends on where you bought the game (`Steam` or `GOG`).
2.  **Go to the RomPatcher.js website:** [https://www.marcrobledo.com/RomPatcher.js/](https://www.marcrobledo.com/RomPatcher.js/)
3.  In the **"ROM file"** field (top), upload your **original** `Indy3D.exe` file from your game's **Resource folder**.
4.  In the **"Patch file"** field (bottom), upload the downloaded `.bps` patch file.
5.  Click the **"Apply patch"** button. The site will prompt you to download the patched file.
6.  **Save** the downloaded file.
7.  **Rename** the downloaded patched file to `Indy3D.exe`.
8.  **Copy** this renamed `Indy3D.exe` into the **Resource** folder of your game, **replacing** the existing file there. *You can delete the old `Indy3D.exe` or keep it as a backup.*

**⚠️ IMPORTANT:** Ensure the new, patched file is named exactly `Indy3D.exe` and is located in the Resource folder. Otherwise, OpenJones might not recognize it. You should now launch the game via `Jones3D.exe` located in the `Resource` folder.

### Step 4: Installing dgVoodoo (Recommended)

Even with OpenJones, you might encounter long loading times or freezes. This is often resolved by using the **dgVoodoo2** wrapper.

1.  **Download dgVoodoo2:** From the official [dgVoodoo2 website](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/). You need the *dgVoodoo v2.86.1*.
2.  **Install:** Follow the instructions for installing dgVoodoo for Infernal Machine. An excellent guide is available in the Steam Community:
    [dgVoodooCpl Installation Guide](https://steamcommunity.com/sharedfiles/filedetails/?id=3281746272)
    *   *Briefly: Copy `dgVoodooCpl.exe`, `dgVoodoo.conf`, and the files from the `MS\x86` folder of the dgVoodoo archive into the `Resource` folder.*
3.  **Configure:** You can use my `dgVoodoo.conf` configuration file `.conf`, which is included in dgvoodoocpl-config folder. Copy it to the `Resource` folder, replacing the existing one, or configure the settings yourself using `dgVoodooCpl.exe`.

**Result:** After completing these steps, the game should launch via `Jones3D.exe` (in the `Resource` folder), utilize OpenJones3D, display the enhanced textures, and run significantly faster and more stably thanks to dgVoodoo.

---

## Tools and Acknowledgements

This mod and its installation were made possible thanks to the following tools and individuals:

*   **Upscaling:**
    *   Main Textures: [Phips/Upscaler](https://huggingface.co/spaces/Phips/Upscaler) on Hugging Face.
    *   Face Restoration: [doevent/Face-Real-ESRGAN](https://huggingface.co/spaces/doevent/Face-Real-ESRGAN) on Hugging Face.
*   **Modding Tools:**
    *   `cndtool`, `matool`, `gobext`: [Urgon (smlu)](https://github.com/smlu/Urgon) - indispensable utilities for working with game resources.
    *   `Indy3DModInstaller`: [the_kovic](https://github.com/thekovic) - a convenient mod installer.
*   **Engine:**
    *   `OpenJones3D`: [Urgon (smlu)](https://github.com/smlu/OpenJones3D) - a modern engine for running the game.
*   **Graphics & Compatibility:**
    *   `dgVoodoo2`: [Dege](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/) - a DirectX wrapper to improve compatibility and performance.

---

## Useful Links

*   [Unpacking Game Resources (Jones3D Docs)](https://github.com/Jones3D-The-Infernal-Engine/Documentation/blob/main/pre-mod.md)
*   [Indy3DModInstaller (the_kovic)](https://github.com/thekovic/Indy3DModInstaller)
*   [Urgon's Utilities (gobext, etc.)](https://github.com/smlu/Urgon)
*   [OpenJones3D Engine (Urgon)](https://github.com/smlu/OpenJones3D)
*   [RomPatcher JS (Online Patcher)](https://www.marcrobledo.com/RomPatcher.js/)
*   [dgVoodoo2 (Website)](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/)
*   [dgVoodoo Installation Guide (Steam)](https://steamcommunity.com/sharedfiles/filedetails/?id=3281746272)
*   [Jones3D - The Infernal Engine Community (Mods, Documentation)](https://github.com/Jones3D-The-Infernal-Engine)
*   [Two Handed Weapon Fix](https://github.com/thekovic/Indy3D-TwoHandFix)
*   [HD Fonts Recreation](https://github.com/Jones3D-The-Infernal-Engine/Fonts-HD-recreation)

---

## Optional: Ready-Made Build

For those who want a fully configured game with this mod, Russian localization, ReShade, and an improved HD font, I have prepared a ready-made configuration of the `Resource` folder.

**Link:** [Google Drive Folder](https://drive.google.com/drive/folders/1aJIOP9-TznFZM4WOWVmuPFvCxx4Twzz2?usp=sharing)

**⚠️ IMPORTANT:** The Google Drive contains two folders:
1.  **`Resource_With_Custom_Level`**: Contains everything mentioned above + an additional custom level from the community ([Original Level](https://github.com/Jones3D-The-Infernal-Engine/Mods)).
2.  **`Resource_Textures_Only_Base`**: Contains only my modified textures and the necessary base files for OpenJones/dgVoodoo, without additional mods like ReShade or custom levels.

**Instructions for the Ready-Made Build:**
1.  Ensure you have completed the [Preparation](#preparation-unpacking-game-resources) (resource unpacking) and [EXE Patching](#step-3-patching-the-executable-downgrade) steps.
2.  Download the contents of one of the folders from Google Drive.
3.  Copy the downloaded `Resource` folder contents into your game's existing `Resource` folder, replacing files when prompted.
