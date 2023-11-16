# MariaDB with Time Zone Docker

This Docker Compose configuration sets up a MariaDB container with time zone support.

## Prerequisites

- Docker installed on your system.

## Usage

1. Clone this repository:

    ```bash
    git clone https://github.com/jr0w3/mariadb-tz-docker.git
    ```

2. Navigate to the cloned directory:

    ```bash
    cd mariadb-tz-docker
    ```

3. Create a `.env` file with the following content:

    ```
    MYSQL_ROOT_PASSWORD=rtpsw
    MYSQL_PASSWORD=psw
    MYSQL_DATABASE=dbname
    MYSQL_USER=user
    ```

   Note: It is strongly recommended to change the passwords to more secure ones.

4. Start the MariaDB container:

    ```bash
    docker-compose up -d
    ```

5. The MariaDB container will now be running. You can connect to it using the configured credentials.

## Configuration

- The `docker-compose.yml` file contains the necessary configuration for the MariaDB container.
- You can adjust environment variables in the `.env` file to customize your MariaDB setup.

## Health Check

The container includes a health check using the `/usr/local/bin/healthcheck.sh` script. It checks the database connection and retries if needed.
