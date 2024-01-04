# Bedrock WordPress Boilerplate with Docker

This repository contains a Bedrock WordPress Boilerplate setup with Docker, providing an easy and modern and flexible environment for WordPress development.

## Quick Start

### Clone the Repository

Start by cloning this repository onto your machine:

```bash
$ git clone https://github.com/agradecido/bedrock-boilerplate.git
```
### Bedrock Boilerplate

After cloning the repository, if you prefer a fresh Bedrock installation instead of using the existing one in the repo, you can delete the 'bedrock' directory and run the following command at the root directory of your repository:

```bash
$ composer create-project roots/bedrock
```

This will create 'bedrock' directory and install a new Bedrock project in.

Or you can update the provided:

```bash
$ cd bedrock
$ composer update
```

- Create a `.env` file for Bedrock. You can use the `.env.example` provided in the Bedrock directory as a template. This file should include:
  - Database credentials (`DB_NAME`, `DB_USER`, `DB_PASSWORD`)
  - WordPress environment settings (`WP_ENV`, `WP_HOME`, `WP_SITEURL`)
  - Authentication unique keys and salts (can be generated using a WordPress salt generator)
  - The database host (and the other database reñated information) in the Bedrock .env file should be set to the name of the SQL container, which will be created by Docker in the subsequent steps.

### Docker Environment

1. Ensure Docker is installed and running on your machine. If you don't have Docker installed, follow [the official Docker installation guide](https://docs.docker.com/engine/install/).
2. Create a `.env` file in 'docker' directory based on the `.env.example` file provided in the repo. This file allows you to configure several aspects of your Docker environment, including:
  - PHP version (e.g., `PHPVERSION=php81`)
  - SQL server version (e.g., `DATABASE=mariadb104`)
  - Credentials for the database (e.g., `MYSQL_ROOT_PASSWORD`, `MYSQL_USER`, `MYSQL_PASSWORD`)
  - Ports for various services
  - Other environment-specific configurations
  - 
## Contributing

Contributions to the Bedrock WordPress Boilerplate are welcome! Here's how you can contribute:

- Fork the repository.
- Create a new branch for your feature or fix.
- Commit your changes and push them to your branch.
- Submit a pull request to merge your changes into the main branch.

## Issues

If you encounter any problems or have suggestions, please open an issue in the repository.
