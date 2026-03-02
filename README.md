# JOKER 777 — Monad Slot Machine

<div align="center">

![JOKER 777 Banner](https://files.catbox.moe/9o0wad.png)

> **Step into the neon-lit world of JOKER 777!**
> Spin the reels, chase the jackpot, and win on-chain NFTs — all on the blazing-fast Monad Mainnet.
>
> 🎰 **Vegas vibes. Neon colors. Real blockchain rewards.** 🎰

[![Monad Mainnet](https://img.shields.io/badge/Network-Monad%20Mainnet-bf00ff?style=for-the-badge)](https://monad.xyz)
[![Chain ID](https://img.shields.io/badge/Chain%20ID-143-00ffff?style=for-the-badge)](https://explorer.monad.xyz)
[![Contract](https://img.shields.io/badge/Contract-0x2d5c...778a-ffd700?style=for-the-badge)](https://explorer.monad.xyz/address/0x2d5ccE1A57eDebcE6c4824e717DfFD84184d778a)

</div>

---

## Features

- 🟣 **Neon UI:** Modern, animated, and responsive slot machine interface.
- 🔵 **Wallet Connect:** Connects to MetaMask or any EIP-1193 compatible wallet.
- 🟡 **Monad Mainnet:** Automatically switches/adds Monad Mainnet (Chain ID: 143).
- 🟣 **Smart Contract:** Interacts with the slot machine contract at `0x2d5ccE1A57eDebcE6c4824e717DfFD84184d778a`.
- 🟡 **Jackpot Pool:** Displays and updates the current jackpot pool.
- 🟣 **Bet Selection:** Choose from allowed bet sizes.
- 🔵 **Spin Animation:** Smooth, staggered per-reel animations.
- 🟡 **Win/Jackpot Detection:** Real on-chain event parsing — detects wins, jackpots, and NFT rewards.
- 🟣 **NFT Badge:** Shows an animated badge when an NFT is minted as a prize.
- 🔵 **Stats & Log:** Tracks spins, wins, total bet, total won, and logs recent results.
- 🟡 **Screen Effects:** Neon flash + emoji rain on win/jackpot.
- 🟣 **Toast Notifications:** Bottom-right popups for all key events.
- 🔵 **Responsive:** Works on desktop and mobile.

---

## How to Play

1. **Open the HTML file** in a browser with MetaMask or another Web3 wallet installed.
2. **Connect your wallet** using the **CONNECT WALLET** button.
3. **Switch to Monad Mainnet** — the app will prompt you automatically if needed.
4. **Select a bet size** from the neon bet buttons.
5. **Press SPIN** and watch the animated reels!
6. **Check your results:**
   - 🟡 **Jackpot?** Neon flash, emoji rain, NFT badge, and a big win!
   - 🟣 **Win?** Celebrate with sound and animation — 2x payout sent!
   - 🔵 **Lose?** Try again — the next spin could be lucky!

### Spin Packages

| Package | Spins | Price |
|---|---|---|
| 🟣 | 100 spins | 1,000 MON |
| 🔵 | 200 spins | 2,000 MON |
| 🟡 | 300 spins | 3,000 MON |
| 🔴 | 400 spins | 5,000 MON |
| 🟢 | 500 spins | 10,000 MON |
| 🌈 | 1,000 spins | 100,000 MON |

---

## Contract Info

| Parameter | Value |
|---|---|
| Contract Address | `0x2d5ccE1A57eDebcE6c4824e717DfFD84184d778a` |
| NFT Contract | `0x17a641607626c243dbaac84AC443801259f0ccF1` |
| Network | Monad Mainnet |
| Chain ID | 143 (`0x8f`) |
| Win Chance | 20% |
| Jackpot Chance | 1% |
| Win Multiplier | 2x |
| Jackpot Fee | 10% of each bet |
| Bet Sizes | 1 MON / 5 MON / 10 MON |

---

## Main Functions (JavaScript)

- **animReel(idx, finalSym, dur)**
  Animates a single reel, ending on the specified symbol.

- **animateReels(s0, s1, s2)**
  Animates all three reels in parallel with staggered stop times, each ending on its final symbol.

- **connectWallet()**
  Connects to the user's wallet, switches/adds Monad Mainnet, and initializes the contract.

- **loadBalance()**
  Fetches and displays the user's MON balance.

- **loadBets()**
  Loads allowed bet sizes from the contract.

- **renderBets()**
  Builds the bet size selection buttons.

- **doSpin() / btnSpin.onclick**
  Sends a spin transaction, waits for confirmation, parses the `Spin` event, animates reels, and updates stats/UI.

- **buyPackage(spins, moons)**
  Purchases a prepaid spin package.

- **updateJackpot() / loadJackpot()**
  Fetches and displays the current jackpot pool from the contract.

- **startJackpotPoll()**
  Periodically updates the jackpot pool every 8 seconds.

- **listenSpinEvents()**
  Listens for `Spin` events from the contract and updates the log for other players' wins in real time.

- **checkNetwork()**
  Verifies the user is on Monad Mainnet (Chain ID 143) and shows the network warning bar if not.

- **showResult(msg, cls)**
  Displays the result message with the appropriate color class.

- **flashScreen(cls)**
  Flashes the screen with a neon effect for win (purple) or jackpot (cyan).

- **startRain(count)**
  Animates falling emoji symbols for win/jackpot celebrations.

- **showNFTBadge(title, sub)**
  Shows an animated badge when an NFT is minted as a prize.

- **addLog(result, amount, cls)**
  Adds a result entry to the spin log (max 20 entries).

- **updateStats()**
  Updates the stats display (spins, wins, total bet, total won).

- **showToast(title, body)**
  Shows a bottom-right toast notification.

- **shortAddr(a)**
  Shortens an Ethereum address for display (e.g. `0x1234...5678`).

- **soundSpin / soundWin / soundJackpot / soundLose()**
  Web Audio API sound effects — no external libraries required.

---

## Files

```
joker777/
├── monad-slot.html       # Main game — single file, no build needed
├── privacy-policy.html   # Privacy policy
└── README.md             # This file
```

---

> **Ready to spin?**
> Connect your wallet, pick your bet, and let the neon reels roll!
>
> _Good luck, and may the JOKER 777 bring you fortune!_ 🃏

---

<div align="center">

## 💜 Support the Project

**Love the game? Help keep the reels spinning!**

Send MON directly on Monad Mainnet:

[![💰 DONATE MON 💰](https://img.shields.io/badge/💰_DONATE_MON_💰-MonadVision-bf00ff?style=for-the-badge&labelColor=000000&color=ffd700)](https://monadvision.com/myspace?feature=Wallet&type=Portfolio)

> Every donation goes directly to the developer wallet on Monad Mainnet.
> Thank you for your support! 🙏

**[👉 Click here to Donate MON](https://monadvision.com/myspace?feature=Wallet&type=Portfolio)**

---

*Joker 777 Slot · Powered by [Monad](https://monad.xyz) · [View Contract](https://explorer.monad.xyz/address/0x2d5ccE1A57eDebcE6c4824e717DfFD84184d778a)*

</div>
