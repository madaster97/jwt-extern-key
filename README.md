# jwt-extern-key
A list of strategies and examples for signing JSON Web Tokens (JWTs) using a private key in a separate, trusted memory location.

## Strategies
- Using a [trusted platform module](https://en.wikipedia.org/wiki/Trusted_Platform_Module) (TPM)
- Using a [hardware security module](https://en.wikipedia.org/wiki/Hardware_security_module) (HSM)
- Using the [Client to Authenticator Protocol](https://en.wikipedia.org/wiki/Client_to_Authenticator_Protocol) (CTAP)

## Examples
### AWS KMS (HSM) - node.js (In Progress)
A node.js service running in AWS, using the [AWS Key Management Service](https://aws.amazon.com/kms/) to protect the key in an HSM managed by AWS

### Windows Cryptography API: Next Generation (TPM) - openssl CLI (In Progress)
The openssl CLI can be used to sign JWTs (see difficulties with Elliptic Curve [here](https://github.com/madaster97/openssl-jws)), and this example using the [openssl-cng-engine](https://github.com/rticommunity/openssl-cng-engine) library to sign JWTs stored in a windows TPM

### Yubikey - Rust application (In Progress)
The [ctap-hid-fido2](https://github.com/gebogebogebo/ctap-hid-fido2) library can interact with a CTAP security key, and this example uses it to sign a JWT 
