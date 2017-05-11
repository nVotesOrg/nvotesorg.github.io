### Welcome to the nVotes project

nVotes is a project for open source, cryptographically secure voting. The following repositories are top-level components.

#### libmix

A mixnet library built on top of [unicrypt](https://github.com/bfh-evg/univote2) and the [univote](https://github.com/bfh-evg/univote2) design. Provides

* A Scala interface to mixnet-based voting system building blocks
* An automatic parallelization mechanism for modPow operations
* A bridge to native gmp implementations for modPow and Legendre
* Patches to the unicrypt library for optimisation (parallelism, native code)
* A benchmark simulating the crypto for a full election cycle

#### nMix

nMix is an open source backend for a mixnet-based, cryptographically secure voting system, featuring strong privacy and verifiability properties. It is a reactive implementation of the core [univote](https://e-voting.bfh.ch/projects/univote/) crypto specification, with a few changes.

The main elements of the cryptographic scheme are

* ElGamal homomorphic distributed cryptosystem[1][5]
* Verifiable re-encryption mixnet with Terelius-Wikstrom shuffles[2][3][6]
* Joint key-generation / decryption with zero knowledge correctness proofs[5]
* Tamper-resistant bulletin board hash-chain[7]
* RSA message signing and trustee authentication[8]