# APIs

## mTLS

The APIs exposed through the `api-mtls.*` domain require the mutual TLS authentication:
* The certificates to authenticate Piattaforma Unitaria are available inside the folder `/certs/inbound-mtls/`
* The systems which requires to communicate through this domain require to communicate their certificates in order to complete the authentication process.

## OAuth2

The REST APIs which are configured with `bearer` security scheme require a token (see [Token Request](#Token%20request)). 

The following SOAP APIs require an `Authorization` header with the same bearer token:
* `Pagamenti Telematici Dovuti Pagati per Ente`
* `Pagamenti Telematici Pagati Riconciliati per Ente`

### Client registration

In order to invoke the `postToken` API, the client needs to be registered on the Piattaforma Unitaria through its web portal, retrieving `client_id` and `client_secret` to be used in the token request.


### Token request

The token to invoke authenticated requests could be obtained through the `postToken` API documented on the `AUTH API` openApi.

EG:
```bash
curl --location --request POST 'https://<PU BASE URL>/pu/auth/oauth/token?grant_type=client_credentials&scope=openid&client_id=<CLIENT_ID>&client_secret=<CLIENT_SECRET>' -d ''
```