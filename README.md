# 🎲 Raffle Smart Contract (Foundry Project)

A decentralized lottery smart contract built with **Solidity + Foundry** using:

* Chainlink VRF (verifiable randomness)
* Chainlink Automation (Keepers)
* Full Foundry test suite with mocks
* Deployment & interaction scripts

This project was created as part of learning smart contract security,
testing, and Chainlink integrations.

---

# ⚙️ Installation & Setup

## 1. Install Foundry (if not installed)

```bash
curl -L https://foundry.paradigm.xyz | bash
foundryup
```

---

## 2. Clone repository

```bash
git clone https://github.com/Bogdan-dev01/raffle-foundry.git
cd raffle-foundry
```

---

## 3. Install dependencies

The `lib/` folder is ignored in GitHub, so you must install dependencies manually:

```bash
forge install
```

This installs:

* forge-std
* Chainlink contracts
* other required libraries

---

## 4. Build project

```bash
forge build
```

---

## 5. Run tests

```bash
forge test -vvvv
```

---

## 6. Coverage (optional)

```bash
forge coverage
```

---

# 🔑 Environment Variables (optional for deployment)

If you plan to deploy to a real network:

Create `.env` file:

```bash
PRIVATE_KEY=your_private_key
RPC_URL=your_rpc_url
ETHERSCAN_API_KEY=optional
```

⚠️ Never commit `.env` to GitHub.

---

# 🚀 Deploy Scripts

Example deployment:

```bash
forge script script/DeployRaffle.s.sol --rpc-url $RPC_URL --private-key $PRIVATE_KEY --broadcast
```

---

# 🧪 Project Structure

```
src/        → Smart contracts
script/     → Deploy + interaction scripts
test/       → Unit tests
lib/        → Dependencies (ignored in git)
broadcast/  → Deploy history (ignored)
```

---

# 🔗 Chainlink Integration Overview

### VRF

Used for provably random winner selection.

### Automation (Keepers)

Automatically triggers winner selection when:

* enough time passed
* players entered
* contract funded

---

# 🛠 Tech Stack

* Solidity 0.8.19
* Foundry
* Chainlink VRF v2.5 mocks
* Forge testing framework

---

# 📚 Learning Goals of This Project

* Smart contract testing (unit + mocks)
* Chainlink VRF integration
* Automation/Keeper logic
* Security-oriented development workflow
* Foundry scripting & deployment flow

---

# ⚠️ Notes

This project is educational and not production audited.
Do not use in production without a professional audit.

---

# 👨‍💻 Author

Solidity / Smart Contract Security learner
Focused on auditing, testing, and DeFi security.
