# Docker skeleton for Symfony

This repository contains a basic Docker Compose structure to start your new Symfony ^5.x project. It has a single container with a PHP 8.0.10 interpreter (you can change the version under `docker/Dockerfile`) and some useful tools like:
- Composer: to install dependencies in your Symfony project
- PHP-CS-FIXER v3: to fix your coding style with a single command (see `Makefile` => `make code-style`)
- Symfony binary: to be able to do things like run a local web server to run your project
- A basic XDEBUG 3 configuration (you can add or remove configuration under `docker/xdebug.ini`)


## Installation
- `make start` to spin up the application container
- `make ssh-be` to access the of the application container's bash

(check other targets in `Makefile`)

Now you can run `symfony` commands to create a new project and so on. (See https://symfony.com/download for more info)

Note: if you get a GIT error during the creation of a new project just set your GITHUB username and email with:
```
git config --global user.name "[your name]"
git config --global user.email "[your email]"
```
or just use the `--no-git` flag (e.g: `symfony new --dir=my-project --no-git`)
