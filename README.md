# eth-rs
Utilities for working with Ethereum addresses in Rust which I have written for an ongoing private project.

Functions:
validate_eth_address returns whether or not a provided Ethereum hexadecimal address is valid by first encoding it into EIP 55 checksum format using eth_checksum_encode and comparing that to the original input -- if the input was a valid address already encoded in checksum form, it returns true; otherwise eth_checksum_encode is passed the checksum and the output compared against it for a final determination

eth_checksum_encode encodes an ethereum address according to the specification laid out in EIP 55 (https://github.com/ethereum/EIPs/blob/master/EIPS/eip-55.md) so that it it is possible to verify that it is a valid address.
