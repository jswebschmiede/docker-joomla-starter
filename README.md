# Joomla Development Environment with Docker

This project provides a Docker-based development environment for Joomla. It allows for quick and easy setup of a Joomla instance with all necessary services. On Windows use it with WSL2.

## Features

-   Joomla CMS
-   MySQL Database
-   phpMyAdmin for database management
-   MailHog for email testing

## Prerequisites

-   Docker
-   Docker Compose
-   Make (optional, but recommended). If not installed on Debian/Ubuntu use `sudo apt-get update && sudo apt-get install make`.

## Quick Start

1. Clone this repository:

    ```
    git clone https://github.com/jswebschmiede/docker-joomla-starter
    cd docker-joomla-starter
    ```

2. Copy the `.env.example` file to `.env` and adjust the values as needed:

    ```
    cp .env.example .env
    ```

3. Start the environment:

    ```
    make up
    ```

4. Open your browser and navigate to:
    - Joomla Frontend: http://localhost:6969
    - Joomla Backend: http://localhost:6969/administrator
    - phpMyAdmin: http://localhost:8080
    - MailHog: http://localhost:8025

## Makefile Commands

-   `make up`: Starts the containers
-   `make start`: Displays information about the running environment
-   `make stop`: Stops the containers
-   `make down`: Stops and removes the containers
-   `make reset`: Removes all containers and local data
-   `make log`: Shows the logs of the containers

## Project Structure

-   `docker-compose.yml`: Defines the Docker services
-   `.env`: Contains environment variables for configuration
-   `Makefile`: Contains useful commands for project management
-   `joomla/`: Directory for Joomla files (created on first start)
-   `db/`: Directory for database files (created on first start)

## Customization

You can customize the configuration in the `.env` file to change ports, versions, and other settings.

## Troubleshooting

If you encounter problems, try the following steps:

1. Stop the containers with `make down`
2. Remove local data with `make reset`
3. Restart the environment with `make up`

If problems persist, check the logs with `make log`.

## Contributing

Contributions are welcome! Please create an issue or pull request for improvement suggestions.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Special Thanks

-   to Christophe Avonture (cavo789) for the original project structure and tutorials
    -   https://www.avonture.be/blog/docker-joomla
    -   https://www.avonture.be/blog/docker-joomla-part-2
