# Basic CRUD app 
This is an example of an on-chain CRUD dapp. This example is a journal dapp where you can create, read, update, and delete journal entries on the solana blockchain and interact with the solana program via a UI. 

## Getting Started

### Prerequisites

- Node v22.14.0
- Rust rustc 1.84.1 (e71f9a9a9 2025-01-27)
- Anchor CLI 0.30.1
- Solana CLI 2.0.24 (src:4c817c28; feat:607245837, client:Agave)

### Installation

#### Clone repo

```shell
git clone <repo-url>
cd <repo-name>
```
```shell
npx create-solana-dapp
cd <project-name>
```
#### Install dependencies

```shell
npm install
```

#### Start the web app

```
npm run dev
```

## Apps

### Anchor

This is a Solana program written in Rust using the Anchor framework.

Note: The solana program code for the journal dapp can be found in `anchor/programs/src/lib.rs`

#### Commands

You can use any normal anchor commands. Either move to the `anchor` directory and run the `anchor` command or prefix the command with `npm run`, eg: `npm run anchor`.

#### Sync the program id:

Running this command will create a new keypair in the `anchor/target/deploy` directory and save the address to the Anchor config file and update the `declare_id!` macro in the `./src/lib.rs` file of the program.

You will manually need to update the constant in `anchor/lib/journal-exports.ts` to match the new program id.

```shell
npm run anchor keys sync
```

#### Build the program:

```shell
npm run anchor-build
```

#### Start the test validator with the program deployed:

```shell
npm run anchor-localnet
```

#### Run the tests

```shell
npm run anchor-test
```

#### Deploy to Devnet

```shell
npm run anchor deploy --provider.cluster devnet
```

### Web

This is a React app that uses the Anchor generated client to interact with the Solana program.

#### Commands

Start the web app

```shell
npm run dev
```

Build the web app

```shell
npm run build
```
