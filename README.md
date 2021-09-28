# API Gateway (Kong) and IAM service (Keycloak)

## Docker Compose resources for the above services <br> <br>

## Prerequisites

- Install [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- Install [Docker](https://www.docker.com/get-docker)
- Install [Docker Compose](https://docs.docker.com/compose/install/#install-compose)

<br>

## Setup

Please follow the steps below in order:

- Configure the service in `kong.yml` file (explanation of each field is provided with an example service)
- Uncomment the database used in Keycloak (PostgreSQL is the default one). <br>
  <strong>Note</strong> - This example is not currently working as MySQL is not ready to receive connections when Keycloak is started.
- Run the Docker Compose using the following command
  `docker-compose up` followed by the `-d` option to run in the detached mode.
- You can access the Keycloak dashboard from the following URL:
  `http://localhost:8080/auth` and login as user 'admin' with password 'Pa55w0rd'
- To register another service, reconfigure the service in the `kong.yml` file and restart the Docker Compose:
  `docker-compose restart`
