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

### 2. Open the project in Visual Studio Code

```bash
cd DEV17-CMS
code .
```

### 3. Start the DevContainer

Inside the vscode, you will be prompted to reopen the project in the DevContainer. Click on the "Reopen in Container" button.
Or open the command palette (`Ctrl+Shift+P`|`Cmd+Shift+P`) and run the command `Remote-Containers: Reopen in Container`.

This project utilize composer to manage dependencies. The DevContainer will install the dependencies and setup the Drupal site for you.
Install the dependencies by running the following command in the vscode integrated terminal:

```bash
composer install
```

Once the dependencies are installed you can access the Drupal site at http://localhost:8080.
