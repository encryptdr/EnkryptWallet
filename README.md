# EnkryptWallet
GIthub Open Source crypto wallet
Privacy Crypto Wallet support unsigned TX

Download: https://enkryptwallet.us/download/EnkryptWalletV1.7.apk



API Tools: supports Partially Signed Bitcoin Transactions (PSBTs)

What Is a Partially Signed Bitcoin Transaction (PSBT)?

A Partially Signed Bitcoin Transaction (PSBT) is a Bitcoin standard that facilitates the portability of unsigned transactions, which allows multiple parties to easily sign the same transaction.

The PSBT standard defines a precise format for conveying Bitcoin transactions. This format can carry metadata about a transaction to make signing and verifying the transaction easier for signers. The standard also defines the process for combining and finalizing transactions, so multiple parties can sign the same transaction in parallel and then combine their respective PSBTs to form a fully signed transaction.

Partially Signed Bitcoin Transactions (PSBTs) allow multiple parties to sign a transaction.
What are Partially Signed Bitcoin Transactions Used For?

Partially Signed Bitcoin Transactions offer several advantages to the Bitcoin community, and makes previously complicated transaction protocols simpler and more easily verifiable.

    Interoperability. PSBTs were originally designed to enhance interoperability between wallets and other Bitcoin software, making transactions more portable between wallets and nodes. PSBT has succeeded to a large extent in gaining industry adoption by all major wallet providers and node softwares.

    Offline Signing. The PSBT format provides useful metadata to assist cold devices in verifying the addresses and amounts being sent in the transaction they are signing. This makes signing a transaction from cold storage more secure, and makes it easier to craft a transaction using a watch-only wallet, sign it using a cold wallet, and broadcast it with a Bitcoin node.

    Multi-Signature Signing. Because PSBT makes a partially signed transaction portable and recognizable, a transaction can be signed by multiple parties or devices easily and securely, making multisig more usable. User friendly multisig will have second-order benefits for the Bitcoin community, including superior privacy, security, and loss prevention.

    Multi-party Transactions. PSBT is particularly useful for coordinating between parties who wish to sign the same transaction. For example, CoinJoin, CoinSwap, and PayJoin protocols require multiple different parties to all sign the same transaction. The PSBT format provides a method for constructing a transaction, passing it between the different signers, and then assembling the final transaction to be broadcast.

How Do Partially Signed Bitcoin Transactions Work?

PSBTs are useful in a variety of cases. For example, in order to construct a CoinJoin transaction with five participants, all five participants would send a message to a coordinator containing some UTXOs they would like to CoinJoin. Each participant would also provide addresses where the CoinJoin transaction should return their bitcoin.

The coordinator would construct a transaction with each of these UTXOs as an input, and create the appropriate outputs to distribute the same amount of bitcoin back to each participant.

Next, the coordinator would convert this transaction to a PSBT, and send the PSBT to each of the five participants. Each participant would separately add their own signatures to the PSBT, and return the PSBTs to the coordinator, who would then combine the five PSBTs, and finalize it. The result would be a fully signed transaction with inputs from each participant.

This process was completely trustless: although each member relied on the coordinator to create and finalize the PSBT, neither the coordinator nor any participant was ever capable of stealing funds from other participants.
Adoption of Partially Signed Bitcoin Transactions

The PSBT standard was defined in BIP 174, and has been widely though not universally adopted by hardware wallets, software wallets, and Bitcoin node software, including Bitcoin Core.

However, the PSBT standard does have several drawbacks, which is why work is currently being done to develop a PSBT v2 standard. In particular, constructing a transaction by adding inputs iteratively is inefficient, and PSBT files can grow relatively large, especially for hardware wallets, which typically have minimal memory.

For the time being, however, PSBT is greatly advancing interoperability between Bitcoin software and hardware, facilitating CoinJoins and other cooperative transaction types, and making multisig easier to use.
