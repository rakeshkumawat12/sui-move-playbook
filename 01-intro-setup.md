# 🚀 Learning Move Smart Contracts with Sui  

Hello, hello! 👋  
Welcome to our journey into learning how to write **Move smart contracts**. This repo will guide you step by step — from setting up your environment to writing your very first Move contract on the **Sui blockchain**.  

---

## 📖 What is Move?  
- **Move** is a smart contract programming language originally developed for the Libra (Diem) project.  
- Today, it’s adopted by **Sui** and **Aptos** blockchains.  
- In this repo, we’ll specifically explore **Move from Sui’s perspective**.  

---

## Getting Started  

### 1. Install Sui CLI  
We’ll need the **Sui CLI** to write, test, and deploy Move contracts.  

- On **macOS** (via Homebrew):  
```bash
brew install sui
sui --version
```

- On Windows:
You may need to install [Chocolatey](https://youtu.be/wW0mXfcC8Sk?si=GWJUV7byWqi8253Y) first.

- On Linux:
Follow the official Sui docs for installation steps.
[Sui CLI Installation Guide](https://docs.sui.io/guides/developer/getting-started/sui-install)

Check if it’s installed properly:
```bash
sui --help
```

### 2. Setup Your First Move Project

Create a working folder for your Move tutorials:

```bash
mkdir move-tut
cd move-tut
```

Initialize a new Move project with Sui:
```bash
sui move <folder-name>
```
Boom! 🎉 You’ve got your first Move project setup.

Resources
- [Sui CLI Installation Guide](https://docs.sui.io/guides/developer/getting-started/sui-install)
- [Move Language Book](https://move-book.com/)
