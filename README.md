# Module-19-Challenge

For this project, I am utilizing Python and Visual Studio to create an application that is integrated with the Ethereum blockchain network. The application allows customers to find fintech professionals, hire them, and pay them with cryptocurrency.

---

## Technologies

This project uses Anaconda, Python, Git Bash, Visual Studio, Github, streamlit, Web3, and Ganache.

---

## Installation Guide

These are the required libraries and dependencies:

    import streamlit as st

    from dataclasses import dataclass

    from typing import Any, List

    from web3 import Web3

    w3 = Web3(Web3.HTTPProvider('HTTP://127.0.0.1:7545'))

    from crypto_wallet import generate_account, get_balance, send_transaction


These are the required libraries and packages to install:

    pip install web3==5.17

    pip install eth-tester==0.5.0b3

    pip install mnemonic

    pip install bip44

---

## Usage

* Step 1: Import Ethereum Transaction Functions into the Fintech Finder Application

I imported the following functions:

    from crypto_wallet import generate_account, get_balance, send_transaction

I created the customer's wallet and account then displayed the balance.

    account = generate_account()

    st.sidebar.write(account.address)

    ether_balance = get_balance(w3, account.address)

    st.sidebar.write(ether_balance)


* Step 2: Sign and Execute a Payment Transaction

I calculated the wage and saved the transaction.

        wage = candidate_database[person][3] * hours

        if st.sidebar.button("Send Transaction"):

        transaction_hash = send_transaction(w3, account, candidate_address, wage)

        st.sidebar.markdown("#### Validated Transaction Hash")

        st.sidebar.write(transaction_hash)


* Screenshots

Web Application:

![Initial Web Interface](https://github.com/abcarmin/Module-19-Challenge/blob/main/Screenshot4.png)


After adding a new block:

![New Blocks Added](https://github.com/abcarmin/Module-19-Challenge/blob/main/Screenshot6.png)


Transaction Details:

![Transaction Details](https://github.com/abcarmin/Module-19-Challenge/blob/main/Screenshot7.png)


Account History:

![Account History](https://github.com/abcarmin/Module-19-Challenge/blob/main/Screenshot8.png)




---

## Contributors

Allyssa Carmin

---

## License

SMU Fintech Course