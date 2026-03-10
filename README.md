# p4pa-api

This repository documents all the information required to communicate with Piattaforma Unitaria.

## APIs

The folder `api` contains the following subdirectories:
* `openAPI`: It contains the specifications of all the APIs provided by Piattaforma Unitaria.
* `wsdl`: It contains the WSDL files of all the SOAP APIs provided by Piattaforma Unitaria.

## Certificates

The folder `certs` contains the following subdirectories:
* `inbound-mtls`: It contains the certificates required to establish a mutual TLS connection required by the APIs exposed by Piattaforma Unitaria through the `api-mtls.*` domain.
* `outbound`: It contains the certificates and IPs used by Piattaforma Unitaria when it invokes external APIs.
