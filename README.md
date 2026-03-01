# JOKER 777 — Monad Slot Machine

![Banner](https://files.catbox.moe/1ueks9.png)

A fully on-chain slot machine game for the Monad Testnet, featuring a neon UI, wallet connection, and NFT rewards.

---

## Features

- **Neon UI:** Modern, animated, and responsive slot machine interface.
- **Wallet Connect:** Connects to MetaMask or any EIP-1193 compatible wallet.
- **Monad Testnet:** Automatically switches/adds Monad Testnet network.
- **Smart Contract:** Interacts with the slot machine contract at `0xE538Abc2a84e51b68d7EE84d8b10E3DF8F9Cf968`.
- **Jackpot Pool:** Displays and updates the current jackpot pool.
- **Bet Selection:** Choose from allowed bet sizes.
- **Spin Animation:** Smooth, performant reel animations.
- **Win/Jackpot Detection:** Detects and displays win/jackpot results, including NFT rewards.
- **NFT Badge:** Shows a badge when an NFT is minted as a prize.
- **Stats & Log:** Tracks spins, wins, total bet, total won, and logs recent results.
- **Accessibility:** Keyboard navigation and focus styles for all interactive elements.
- **Responsive:** Works on desktop and mobile.

---

## How to Use

1. **Open the HTML file** in a browser with MetaMask or another Web3 wallet installed.
2. **Connect your wallet** using the "CONNECT WALLET" button.
3. **Select a bet size** from the available options.
4. **Press "SPIN"** to play the slot machine.
5. **View results, stats, and logs** as you play. Win or jackpot results will trigger special effects and may mint an NFT to your wallet.

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

## Banner

The banner image is displayed at the top of the page:

```html
<img src="https://files.catbox.moe/1ueks9.png" alt="JOKER 777 Banner" style="width:100%;max-width:900px;display:block;margin:24px auto 0;box-shadow:0 0 32px #ff2d9b55;border-radius:12px;">
