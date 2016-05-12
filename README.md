# mocks
Mocked services needed for STUPS infrastructure:

* OAuth2 Provider: generate and validate OAuth2 access tokens
* Service User API: manage OAuth2 service users
* Team Service: list teams and get team membership
* Token Service: generate OAuth2 access tokens for employees

Every mock should be available as a runnable Docker image:

    $ docker run registry.opensource.zalan.do/stups/mock-team-service:0.1
