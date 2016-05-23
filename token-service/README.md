# Token Service Mock

Retrieves a token from the OAuth2 Authorization Server (mock) using password grant. Provide resource owner credentials as Basic Auth.

## Usage

The token service is accessible at port 3002.

With node

    git checkout https://github.com/zalando-stups/mocks/tree/master/token-service
    cd token-service/src
    node app.js

With Docker

    docker run registry.opensource.zalan.do/stups/mock-token-service:0.1

### Accepted environment variables

* `OAUTH_AUTH_URL` (required): URL of the `access_token` endpoint of the authorization server.
* `OAUTH_CREDENTIALS` (required): Client ID and secret to use at authorization server in the format "id=secret".

## API

See [swagger.yml](swagger.yml).