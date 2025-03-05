# Platform requirements 

This document lists all the necessary requirements for complying to a C2PA compliant platform.

## Cryptopgraphy & Key Management

* The platform should provide support for following minimum Hashing Algorithms
  1. SHA-256
  2. SHA-384
  3. SHA-512

* The platform should provide support for following minimum Signing Algorithms
  1. ES256 (ECDSA with SHA-256)
  2. ES384 (ECDSA with SHA-384)
  3. ES512 (ECDSA with SHA-512)
  4. PS256 (RSASSA-PSS using SHA-256 and MGF1 with SHA-256)
  5. PS384 (RSASSA-PSS using SHA-384 and MGF1 with SHA-384)
  6. PS512 (RSASSA-PSS using SHA-512 and MGF1 with SHA-512)
  7. EdDSA (Edwards-Curve DSA).
  Note for EdDSA  Ed25519 instance only. No other EdDSA instances are allowed.

* Support for Signing Key confidentiality protection
The platform MUST support Key protection from key loss or key theft

* Support for Signing Key rotation

* Support for Signing Key revocation

* Support for export of Public Part of Signing Key to external clients requesting this information

## Secure Storage

* Platform MUST provide a secure storage to Assertions and Claims prior to signing

## Attestation

* Platform MUST support Remote Attestation of the platform running the Claim Generator Application

* Platform MUST support the Key Attestation of the Claim Signing Key

* Platform MUST provide API to export Remote Attestation Results/Verdict to the requesting Client on the Device, including the Claim Generator

## Secure Communication

* Secure TLS V1.3 Communication from a TEE to remote locations for Certificate Signing Requests

* Adherence to the C2PA proposed protocol while making such requests

## Claim Generator

* Platform allows flexibility to run part of the Claim Generator Application to run inside a TEE or a Secure Environment

* Platform support strong binding of Claim Generator 

## Compliance

* Support for Platform Compliance as mandated by C2PA consortium - This requirement is TBD at the moment
