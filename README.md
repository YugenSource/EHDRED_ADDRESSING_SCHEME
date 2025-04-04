# EHDRED_ADDRESSING_SCHEME
The EHDRED Addressing Scheme

## Abstract

There comes a time where there needs to be a new, novel method of addressing schemes for addresses that is cross-compatabile with other addresses.

We introduce the `Ehdred Addressing Scheme`, an addressing scheme that uses subgroups and protocol brackets to name the protocol, prefixes for addresses with subgroups, and suffixes for variables or actions. It uses a 224-bit digest using blake2s (so favorable for IoT and smaller bit devices) or SHA3 (keccak) to produce the desired address from inputs which can be anything. The address can be encoded in hexadecimal or base58.



## Input For Address

The typical input to create an address is a public key but can vary. It needs to be put in as bytes.

## Examples

```
EXAMPLE: [EHDRED]::[Request]addr_a4e42acf366bdd395b8403def744420bb550312a5354585057aadd1e?p=1,sec="STRICT"@sec7

PROTO: [EHDRED]
PROTO-WITH-SUBGROUP: [EHDRED]::[REGISTER]
ADDR_PREFIX: addr_
ADDR_PREFIX-WITH-SUBGROUP: addr::cert_
ADDRESS (224-bit BLAKE2s or SHA3): a4e42acf366bdd395b8403def744420bb550312a5354585057aadd1e
SUFFIX: ?
VARIABLES: p=1,sec="STRICT"
ACTION: @
ACTION-TYPES: sec7 (strict-security)
```
