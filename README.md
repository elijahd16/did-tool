# did-tool – Proof-of-Concept for BSc IT Management for Business Report

This repo contains the **did-tool** prototype evaluated in my report.
*"Governing AI Agent Ecosystems: Discovery, Reputation and Verification in the A2A and MCP Protocol Context."*.

## Thesis context
The code was subjected to a Failure-Mode & Effects Analysis (FMEA) to expose
real-world risks in DID/VC verification (see report sections 3.4.2 & 4.4.2).
Critical findings (expired-VC acceptance, revocation lag, etc.) are derived
directly from the unit tests in this repo.

## Functions used in the study
* `did_generate.py` – creates `did:key` identifiers (Ed25519)  
* `vc_sign.py`   – issues Verifiable Credentials (JSON-LD & JWT)  
* `vc_verify.py`  – verifies signatures and basic structure  
* `tests/`    – pytest cases that drove the FMEA

## Quick start
```bash
git clone https://github.com/elijahd16/did-tool.git
cd did-tool
poetry install
poetry run pytest     # reproduces all FMEA test cases
```

## Dependencies
cryptography, jwcrypto, pyld==2.0.3, pydantic, py-multibase, py-multicodec.

## License
Apache-2.0