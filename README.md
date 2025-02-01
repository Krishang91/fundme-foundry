


## **📜 FundMe - A Smart Contract for Crowdfunding**
A decentralized crowdfunding smart contract built on Ethereum using **Foundry** for testing and deployment.

---

## **🚀 Features**
- Users can **fund** the contract with ETH.
- The contract **tracks** the total funds and contributors.
- Only the **owner** (deployer) can **withdraw** the funds.
- Integrated with **Chainlink Price Feeds** for ETH/USD conversion.
- Fully tested using **Foundry** (Forge & Cast).

---

## **📂 Project Structure**
```
📦 fundme-foundry
 ┣ 📂 contracts            # Solidity smart contracts
 ┃ ┣ 📜 FundMe.sol         # Main crowdfunding contract
 ┃ ┗ 📜 MockV3Aggregator.sol  # Mock Chainlink Price Feed (for tests)
 ┣ 📂 script               # Deployment scripts
 ┃ ┣ 📜 DeployFundMe.s.sol # Deployment script using Forge
 ┣ 📂 test                 # Unit tests
 ┃ ┣ 📜 FundMeTest.t.sol   # Test cases using Foundry
 ┣ 📜 foundry.toml         # Foundry configuration file
 ┣ 📜 .env                 # Environment variables (RPC URL, private key)
 ┗ 📜 README.md            # Project documentation
```

---

## **⚙️ Prerequisites**
- **Foundry** (Install using `curl -L https://foundry.paradigm.xyz | bash`)
- An Ethereum Sepolia RPC Provider (**Alchemy or Infura**)
- A wallet with **Sepolia ETH** (for testing)

---

## **🛠 Installation & Setup**
### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/your-username/fundme-foundry.git
cd fundme-foundry
```

### **2️⃣ Install Foundry**
```bash
foundryup
```

### **3️⃣ Set Up Environment Variables**
Create a `.env` file:
```bash
SEPOLIA_RPC_URL="https://eth-sepolia.alchemyapi.io/v2/YOUR_API_KEY"
PRIVATE_KEY="YOUR_WALLET_PRIVATE_KEY"
ETHERSCAN_API_KEY="YOUR_ETHERSCAN_API_KEY"
```

### **4️⃣ Build the Contracts**
```bash
forge build
```

### **5️⃣ Run Tests**
```bash
forge test -vvvv
```

### **6️⃣ Deploy to Sepolia**
```bash
make deploy-sepolia
```
or manually:
```bash
forge script script/DeployFundMe.s.sol:DeployFundMe --rpc-url $SEPOLIA_RPC_URL --private-key $PRIVATE_KEY --broadcast --verify --etherscan-api-key $ETHERSCAN_API_KEY -vvvv
```

---

## **🧪 Testing**
Run all unit tests:
```bash
forge test
```
For detailed output:
```bash
forge test -vvvv
```

---

## **📜 Contract Details**
### **FundMe.sol**
- `fund()` → Allows users to send ETH.
- `withdraw()` → Only the owner can withdraw funds.
- `getConversionRate()` → Fetches ETH/USD price from Chainlink.

---

## **🔗 Useful Links**
- [Foundry Documentation](https://book.getfoundry.sh/)
- [Ethereum Sepolia Faucet](https://sepoliafaucet.com/)
- [Chainlink Price Feeds](https://docs.chain.link/data-feeds/)

---

## **🛠 Future Improvements**
- Implement **refund** functionality.
- Support **multiple funding campaigns**.
- Add a **frontend** using React & Ethers.js.

---

## **💡 Contributing**
Feel free to submit **issues** and **pull requests** to improve the contract.

---

## **📜 License**
This project is licensed under the **MIT License**.

---

