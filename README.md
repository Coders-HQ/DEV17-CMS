# DEV 17 CMS

A Drupal based project to support the back end and managing permissions.
To be extended with other projects

> THis Document is a work in progress and will be updated with more detailed usage and setup.

## Setup

This project utilize DevConainers as a development environment. To get started, you need to have Docker and Visual Studio Code installed.

- Install Docker: https://docs.docker.com/get-docker/
- Install Visual Studio Code: https://code.visualstudio.com/

### 1. Clone the repository

```bash
git clone https://github.com/Coders-HQ/DEV17-CMS.git
```

### 2. Update the submodule to latest

```bash
git submodule update --rebase
```

### 2. Open the project in Visual Studio Code

```bash
cd DEV17-CMS
code .
```

### 3. Start the DevContainer

Inside the vscode, you will be prompted to reopen the project in the DevContainer. Click on the "Reopen in Container" button.
Or open the command palette (`Ctrl+Shift+P`|`Cmd+Shift+P`) and run the command `Remote-Containers: Reopen in Container`.
Also to force the recreaction of the devcontainer you can run the command `Remote-Containers: Rebuild and Reopen in Container`.

This project utilize composer to manage dependencies. The DevContainer will install the binaries and extentions required for the project including nodejs, npm, and composer.

For PHP, install the dependencies by running the following command in the vscode integrated terminal:

```bash
composer install
```

Once the dependencies are installed you can access the Drupal site at http://localhost:8080.

### Demo Site

As this is work in progress Drupal offers a demo site that you can test for that when running
the installation wizard you can select `Demo: Umami Food Magazine (Experimental)` under Choose profile.

#### Database configuration

For the setup database, the devcontainer will spin a MySQl database and you can use the following credentials from `devcontainer.env`:

- Database type: MySQL, MariaDB, Percona Server, or equivalent
- Database name: `db`
- Database user: `drupal`
- Database password: `drupalPASS`
- Expand advanced options and for *Host*: `database`

## Update DevContainer images

- To pull the latest MySQL and drupal-devcontainer images run the following command:

```bash
cd .devcontainer
docker-compose pull
```
