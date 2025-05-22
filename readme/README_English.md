This mod replaces the original game textures of **Indiana Jones and the Infernal Machine** with improved textures created using AI upscaling. The goal is to enhance the game's visual quality on modern displays. **This guide will also cover the installation** of improved sounds and the **modern** OpenJones3D engine.

## ⚠️ Disclaimer

*   **Rights:** The original assets and the game Indiana Jones and the Infernal Machine are the property of their respective rights holders (Lucasfilm Games / Disney, etc.). I do not claim ownership of the original materials. This mod is a derivative work.
*   **Usage:** This texture pack is provided "as-is" exclusively for personal, non-commercial use by fans of the game who own a legal copy of Indiana Jones and the Infernal Machine.
*   **Liability:** You use these textures at your own risk. The mod author is not responsible for any potential issues with the game or your computer.
*   **Distribution:** Any commercial use of these improved textures is prohibited. When distributing the mod or its derivative versions (if permitted), you must credit the author of the **upscaling** and maintain its non-commercial nature.
*   **Status:** The mod author is not affiliated with the game's developers or publishers.

---

## Contents

*   [Requirements](#requirements)
*   [Preparation: Unpacking Game Resources](#preparation-unpacking-game-resources)
*   [Mod Installation](#mod-installation)
    *   [Step 1: Texture Installation](#step-1-texture-installation)
    *   [Step 2: OpenJones3D Engine Installation (Required)](#step-2-openjones3d-engine-installation-required)
    *   [Step 3: Patching the Executable File (Downgrade)](#step-3-patching-the-executable-file-downgrade)
    *   [Step 4: dgVoodoo Installation (Recommended)](#step-4-dgvoodoo-installation-recommended)
    *   [Step 5: 3D Sound Installation (Recommended)](#step-5-3d-sound-installation-recommended)
    *   [Step 6: Improved Sounds Installation (Recommended)](#step-6-improved-sounds-installation-recommended)
    *   [Step 7: ReShade Installation (Optional)](#step-7-reshade-installation-optional)
*   [Tools and Acknowledgements](#tools-and-acknowledgements)
*   [Useful Links](#useful-links)
*   [Additionally: Pre-configured Build](#additionally-pre-configured-build)

---

## Requirements

*   A legal copy of the game **Indiana Jones and the Infernal Machine**.
*   **Unpacked game resources.** See the [Preparation](#preparation-unpacking-game-resources) section below.

---

## Preparation: Unpacking Game Resources

Before installing any mods, including this one, you need to extract (unpack) **the contents of the game archives (`.gob` files) from the `Resource` folder into their respective subfolders within it.**

**There are two main ways to do this:**

1.  **Manual method:** Follow the detailed instructions on the Jones3D community GitHub:
    [Resource Unpacking Instructions](https://github.com/Jones3D-The-Infernal-Engine/Documentation/blob/main/pre-mod.md)
    *(This method requires using the `gobext` and `cndtool` utilities by Urgon).*

2.  **Using Indy3DModInstaller:** Use the utility by the_kovic, which automates the process. This is usually faster and more convenient.
    *   Download: [Indy3DModInstaller](https://github.com/thekovic/Indy3DModInstaller)
    *   Run the installer, following its instructions as specified in the *README*.

**Important:** After unpacking, the original `CD1.gob`, `CD2.gob`, and `JONES3D.gob` files will no longer be used directly by the game. Instead, the game will read files from the folders inside `Resource`.

---

## Mod Installation

### Step 1: Texture Installation

Once the game resources are unpacked:

1.  **Download** the `main-upscaled-textures` and `bmp-upscaled-textures` folders with AI-upscaled textures from this repository.
2.  **Choose an installation method:**
    *   **Via Indy3DModInstaller:** If you are using this installer, point it to the path of the downloaded texture folders. It should place the files correctly.
    *   **Manually:** Unpack the texture archive. Copy all files from the archive into your game's `mat` folder, agreeing to replace files when prompted.
3.  After successfully installing the textures, you need to choose a language pack from the `localizations` folder in **this** repository. After selecting the language folder, you only need to **copy its contents** into the `Resource` folder.

---

### Step 2: OpenJones3D Engine Installation (Required)

Standard game launch with unpacked resources is only possible in developer mode (see Toggle Dev Mod in Indy3DModInstaller), otherwise the game will ask for the disc. To bypass this, it is highly recommended to install **OpenJones3D** — a modern open-source engine for the game by Urgon.

1.  Go to the [OpenJones3D](https://github.com/smlu/OpenJones3D) repository page.
2.  Download the latest version (usually a zip archive). Alternatively, you can download the latest version via `Releases`.
3.  **Extract the contents of the downloaded archive** directly into the `Resource` folder, agreeing to replace files.

**⚠️ CAUTION! BUG!:** *Do not copy* the `gen_fadeplate.3do` file from the archive into your game's `Resource/mat` folder.** This file can cause a bug where the screen borders move your Jones. I'm not kidding - on one of the levels, it might just push him off.

### Step 3: Patching the Executable File (Downgrade)

---

OpenJones3D requires the original game executable file (`Indy3D.exe`) to be downgraded to version 1.0.

1.  **Find the downgrade files:** In this repository's files, there should be a `downgrade-file` folder containing `.bps` files. **The choice of the correct `.bps` file** depends on where you bought the game (`Steam` or `GOG`).
2.  **Go to the RomPatcher.js website: [https://www.marcrobledo.com/RomPatcher.js/](https://www.marcrobledo.com/RomPatcher.js/)
3.  In the "ROM file" field (top), upload your **original** `Indy3D.exe` file from the `Resource` folder.
4.  In the "Patch file" field (bottom), upload the `.bps` patch file **corresponding to your game version**.
5.  Click the "Apply patch" button. The site will offer to download the patched file.
6.  **Save** the downloaded file.
7.  **Rename** the downloaded patched file to `Indy3D.exe`.
8.  **Copy** this renamed `Indy3D.exe` into the `Resource` folder, **replacing** the existing file there. *The old `Indy3D.exe` can be deleted or saved as a backup.*

**⚠️ IMPORTANT:** Ensure the new, patched file is named exactly `Indy3D.exe` and is located in the `Resource` folder. Otherwise, OpenJones3D may not recognize it. You can now run the game via `Jones3D.exe` from the `Resource` folder.

---

### Step 4: dgVoodoo Installation (Recommended)

Even with OpenJones**3D**, you might encounter long loading times or freezes. This is often resolved by using the **dgVoodoo2** wrapper.

#### Path A:

1.  **Download dgVoodoo2:** From the official [dgVoodoo2 website](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/). You need version *dgVoodoo v2.86.1* (or newer, if available and compatible).
2.  **Install:** Follow the dgVoodoo installation instructions for Infernal Machine. An excellent guide is available on Steam:
    [dgVoodooCpl Installation Guide](https://steamcommunity.com/sharedfiles/filedetails/?id=3281746272)
    *   *Briefly: Copy `dgVoodooCpl.exe`, `dgVoodoo.conf` (if you have a ready-made one), and files from the `MS\x86` folder of the dgVoodoo archive into the `Resource` folder.*
3.  **Configure:** You can use **my** `dgVoodoo.conf` configuration, located in the `dgvoodoocpl-config` folder of **this repository**, and copy it to the `Resource` folder, replacing the existing one, or configure the settings yourself via `dgVoodooCpl.exe`.

**Result:** After completing these steps, the game should launch via `Jones3D.exe` (in the `Resource` folder), use OpenJones3D, display improved textures, and run significantly faster and more stably thanks to dgVoodoo.

**⚠️ VERY IMPORTANT:** In the **Steam guide**, be sure to download and **copy** the `dinput.dll` file to the `Resource` folder, otherwise you will have a problem with the *Save* button (yes, this is the only button that behaves very strangely).

#### Path B: Download all files, except for the `PNG` images, from the **`dgvoodoocpl-config` folder of this repository** and **copy** them into the `Resource` folder.

---

### Step 5: 3D Sound Installation (Recommended)

1.  **Download:** From the **main folder of this repository**, download the `3D-sound` folder and **copy the necessary files from there (e.g., `dsound.dll`, `dsoal-config.ini`)** into your game's `Resource` folder.
2.  **Install OpenAL:** Open/unpack the `oalinst.zip` archive and run the OpenAL installer.

---

### Step 6: Improved Sounds Installation (Recommended)

1.  **Download:** From the **main folder of this repository**, download the `high-quality-sounds` folder.
2.  **Install:** **Copy** all files from the `high-quality-sounds` folder into `Resource\sound` (this should **replace** 1540 files).

**⚠️ DISCLAIMER:** During sound improvement, an **experimental** AI *'versatile_audio_super_resolution'* was used. Not all files were processed due to terrible interference or complete silence. Soundtracks were NOT processed due to the same issue.

---

### Step 7: ReShade Installation (Optional)

1.  **Download the latest version of ReShade:** From the official [ReShade website](https://www.reshade.me/#download).
2.  **Install:** Click on the installation file and select the `Jones3D.exe` file (the path should be something like: `path-to-your-game-folder\Resource\Jones3D.exe`). However, you can also install ReShade on `Indy3D.exe`. **No significant** difference has been **noticed**.
3.  **Select:** From the offered *rendering APIs*, click on DirectX 10/11/12.
4.  **Next:** You can select `fx` **to your liking** and start playing after installation, or after installation, download the `reshade` folder from **this repository** with working shaders **tested by me** and **copy** the `reshade-shaders` folder into the `Resource` folder **ONLY** after installing the main ReShade.

---

## Tools and Acknowledgements

This mod and its installation were made possible thanks to the following tools and people:

*   **Texture Upscaling:**
    *   Main textures: [Phips/Upscaler](https://huggingface.co/spaces/Phips/Upscaler) on Hugging Face.
    *   Face restoration: [doevent/Face-Real-ESRGAN](https://huggingface.co/spaces/doevent/Face-Real-ESRGAN) on Hugging Face.
*   **Modding Tools:**
    *   `cndtool`, `matool`, `gobext`: [Urgon (smlu)](https://github.com/smlu/Urgon) — indispensable utilities for working with game resources.
    *   `Indy3DModInstaller`: [the_kovic](https://github.com/thekovic) — a convenient mod installer.
*   **Engine:**
    *   `OpenJones3D`: [Urgon (smlu)](https://github.com/smlu/OpenJones3D) — a modern engine for running the game.
*   **Graphics and Compatibility:**
    *   `dgVoodoo2`: [Dege](http://dege.freeweb.hu/dgVoodoo2/dgVoodoo2/) — DirectX wrapper for improving compatibility and performance.
*   **3D Sound:**
    *   `OpenAL`: [OpenAL](https://openal.org/downloads/) — a cross-platform audio application programming interface.

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
*   [Fix for Two-Handed Weapons](https://github.com/thekovic/Indy3D-TwoHandFix)
*   **[Instructions for restoring 3D sound (Russian only)](https://www.ixbt.com/live/games/kak-aktivirovat-eax-dlya-staryh-igr-v-windows-10.html)**

---

**⚠️ Still have questions?** [Join the Indy3D Community server](https://discord.gg/rhQfrWB)