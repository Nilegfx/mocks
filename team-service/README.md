# Team Service Mock

Knows users, their teams and the cloud accounts they have access to.

## Usage

The team service is accessible at port 3001.

With node

    git checkout https://github.com/zalando-stups/mocks/tree/master/team-service
    cd team-service/src
    node server.js

With Docker

    docker run registry.opensource.zalan.do/stups/mock-team-service:0.1

For the docker client to be able to read the CSV files, you have to make them accessible via a volume:

    docker run -d -e USER_SOURCE=user.csv -e TEAM_SOURCE=team.csv -e DATA_DIR=/data -p 3001:3001 -v /data:<DATA_DIR> registry.opensource.zalan.do/stups/mock-team-service:0.1

### Accepted environment variables

* `DATA_DIR` (required): Absolute path of a directory where user and team source (see next) are located.
* `USER_SOURCE` (required): Name of a CSV file where user and their team are listed
* `TEAM_SOURCE` (required): Name of a CSV file where the teams and their cloud account id are listed.
* `TOKENINFO_URL`: URL of /tokeninfo endpoint to check OAuth2 access tokens. If it's not present, requests will not be checked for tokens.

## File formats

### user.csv

    # user id, team id
    npiccolotto,stups
    test,stups
    iam,greendale

### team.csv

    # team id, description, cloud account id, dn
    stups,Cloud Engineers,84849249,some-dn
    greendale,Identity Managers,5813148535,other-dn

## API

See [swagger.yml](swagger.yml).