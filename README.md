
# **SIGHTED Cross-Chain Swap (XSC) – ICP ↔ Calimero**

This project implements **cross-chain swaps (XCS)** for **fungible tokens (FTs)** between **Internet Computer Protocol (ICP)** and **Calimero private shards**. The swap system allows seamless token movement and balance management across the two networks, leveraging **Chain Key Cryptography (CKC)** on ICP and Calimero's private data management.

---

## **Features**
- **Cross-Chain Token Swapping**: Supports token swaps between ICP and Calimero shards.
- **Token Balance Tracking**: Query real-time balances on both ICP and Calimero.
- **Secure Token Storage**: Calimero private shards for secure and private data management.
- **Interoperability**: Designed for seamless cross-chain communication and token exchange.

---

## **Installation**

### Prerequisites
- **DFX CLI**: For deploying and managing ICP canisters. [Install DFX CLI](https://internetcomputer.org/docs/current/developer-docs/setup/install/)  
- **Node.js**: For integrating the Calimero SDK in the frontend (optional for full implementation).

---

### **Steps to Run Locally**
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-repo/xsc-icp-calimero.git
   cd xsc-icp-calimero
   ```

2. **Start the Local DFX Replica**:
   ```bash
   dfx start --background
   ```

3. **Build and Deploy the Canisters**:
   ```bash
   dfx deploy
   ```

---

## **Usage**

### Deposit Tokens to ICP
```bash
dfx canister call xsc depositICP '(principal "user-principal-id", 1000)'
```

### Swap Tokens from ICP to Calimero SHARD
```bash
dfx canister call xsc swapToCalimero '(principal "user-principal-id", 500)'
```

### Swap Tokens from Calimero SHARD to ICP
```bash
dfx canister call xsc swapToICP '(principal "user-principal-id", 200)'
```

### Check Token Balance
```bash
dfx canister call xsc balance '(principal "user-principal-id")'
```

---

## **Development**

1. **Build the Contracts**:
   ```bash
   dfx build
   ```
2. **Run Tests**:
   ```bash
   dfx test
   ```

---

## **Future Enhancements**
1. **Calimero SDK Integration**: Use the Calimero TypeScript SDK for token verification and private data management.
2. **Real-Time Balance Updates**: Enable WebSocket communication for live updates.
3. **Token Verification**: Add ECDSA signature verification for swap confirmation.
