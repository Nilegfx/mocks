This is just a copy of https://github.com/zalando-incubator/mocks
changes: 
* OAuth2 Provider:
    - use port **7002** other than the commonly used 3000!
    - send **scope** back along with the token and rest of info

# mocks
Mocked services needed for STUPS infrastructure:

* OAuth2 Provider: generate and validate OAuth2 access tokens
* Service User API: manage OAuth2 service users
* Team Service: list teams and get team membership
* Token Service: generate OAuth2 access tokens for employees

Every mock should be available as a runnable Docker image:

    $ docker run registry.opensource.zalan.do/stups/mock-team-service:0.1
