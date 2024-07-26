---
term: RICOCHET
---

A technique involving conducting multiple fake transactions to oneself to simulate a transfer of ownership of bitcoins. Ricochet is used to blur the specifics that could compromise the fungibility of a Bitcoin coin. For example, if you perform a coinjoin, your output coin will be identified as such. This label of a "_coin from a coinjoin_" can affect the fungibility of a UTXO. Regulated entities, such as exchange platforms, may refuse to accept a UTXO that has undergone a coinjoin, or even demand explanations from its owner, with the risk of having their account blocked or their funds frozen. In some cases, the platform may even report your behavior to state authorities. This is where the Ricochet method comes into play. To obscure the trace left by a coinjoin, Ricochet executes four successive transactions where the user transfers their funds to themselves at different addresses. After this sequence of transactions, the Ricochet tool finally routes the bitcoins to their final destination, such as an exchange platform. The goal is to create distance between the original coinjoin transaction and the final spending act. In this way, chain analysis tools will likely assume that there has been a transfer of ownership after the coinjoin, and therefore it is unnecessary to initiate actions against the issuer. The most common use case for Ricochet occurs when it is necessary to conceal prior participation in a coinjoin on a UTXO, especially to avoid being targeted by AML/CTF policies of regulated platforms or blacklists. The Ricochet tool is available on the Samourai Wallet.