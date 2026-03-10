# APIs

# mTLS

The APIs exposed through the `api-mtls.*` domain require the mutual TLS authentication:
* The certificates to authenticate Piattaforma Unitaria are available inside the folder `/certs/inbound-mtls/`
* The systems which requires to communicate through this domain require to communicate their certificates in order to complete the authentication process.

# OAuth2

The APIs which are configured with `bearer` security scheme require a token obtained through the `postToken` API documented on the `AUTH API` openApi. 