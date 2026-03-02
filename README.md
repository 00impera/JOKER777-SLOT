# JOKER 777 — Monad Slot Machine

![JOKER 777 Banner](https://files.catbox.moe/9o0wad.png)

> **Step into the neon-lit world of JOKER 777!**  
> Spin the reels, chase the jackpot, and win on-chain NFTs — all on the blazing-fast Monad Testnet.  
>  
> 🎰 **Vegas vibes. Neon colors. Real blockchain rewards.** 🎰

---

## Features

- 🟣 **Neon UI:** Modern, animated, and responsive slot machine interface.
- 🔵 **Wallet Connect:** Connects to MetaMask or any EIP-1193 compatible wallet.
- 🟡 **Monad Testnet:** Automatically switches/adds Monad Testnet network.
- 🟣 **Smart Contract:** Interacts with the slot machine contract at `0xE538Abc2a84e51b68d7EE84d8b10E3DF8F9Cf968`.
- 🟡 **Jackpot Pool:** Displays and updates the current jackpot pool.
- 🟣 **Bet Selection:** Choose from allowed bet sizes.
- 🔵 **Spin Animation:** Smooth, performant reel animations.
- 🟡 **Win/Jackpot Detection:** Detects and displays win/jackpot results, including NFT rewards.
- 🟣 **NFT Badge:** Shows a badge when an NFT is minted as a prize.
- 🔵 **Stats & Log:** Tracks spins, wins, total bet, total won, and logs recent results.
- 🟡 **Accessibility:** Keyboard navigation and focus styles for all interactive elements.
- 🟣 **Responsive:** Works on desktop and mobile.

---

## How to Play

1. **Open the HTML file** in a browser with MetaMask or another Web3 wallet installed.
2. **Connect your wallet** using the <span style="color:#00ffff"><b>CONNECT WALLET</b></span> button.
3. **Select a bet size** from the neon bet buttons.
4. **Press <span style="color:#bf00ff"><b>SPIN</b></span>** and watch the animated reels!
5. **Check your results:**  
   - 🟡 **Jackpot?** Neon flash, NFT badge, and a big win!  
   - 🟣 **Win?** Celebrate with sound and animation.  
   - 🔵 **Lose?** Try again — the next spin could be lucky!

---

## Main Functions (JavaScript)

- **buildReels()**  
  Initializes the slot machine reels with random symbols.

- **animReel(idx, finalSym, dur)**  
  Animates a single reel, ending on the specified symbol.

- **animateReels(s0, s1, s2)**  
  Animates all three reels in parallel, each ending on its final symbol.

- **connectWallet()**  
  Connects to the user's wallet, switches/adds Monad Testnet, and initializes the contract.

- **updateWalletUI()**  
  Updates wallet address, balance, and UI states after connection.

- **setSpinReady()**  
  Sets the spin button and UI to the ready state.

- **loadBets()**  
  Loads allowed bet sizes from the contract.

- **buildBetButtons()**  
  Builds the bet size selection buttons.

- **doSpin()**  
  Sends a spin transaction, waits for confirmation, parses results, animates reels, and updates stats/UI.

- **setSpinSpinning(isSpinning)**  
  Sets the spin button and UI to the spinning/loading state.

- **updateJackpot()**  
  Fetches and displays the current jackpot pool from the contract.

- **startJackpotPoll()**  
  Periodically updates the jackpot pool.

- **listenSpinEvents()**  
  Listens for Spin events from the contract and updates the log for other players' wins.

- **showResult(msg, cls)**  
  Displays the result message with animation.

- **flashScreen(cls)**  
  Flashes the screen with a neon effect for win/jackpot.

- **startRain(count)**  
  Animates falling symbols for win/jackpot.

- **showNFTBadge(title, sub)**  
  Shows a badge when an NFT is minted as a prize.

- **addLog(result, amount, cls)**  
  Adds a result entry to the spin log.

- **updateStats()**  
  Updates the stats display (spins, wins, total bet, total won).

- **showToast(title, body)**  
  Shows a toast notification.

- **shortAddr(a)**  
  Shortens an Ethereum address for display.

- **loadEthers()**  
  Loads Ethers.js v6 from CDN if not already loaded.

---

> **Ready to spin?**  
> Connect your wallet, pick your bet, and let the neon reels roll!  
>  
> _Good luck, and may the JOKER 777 bring you fortune!_
