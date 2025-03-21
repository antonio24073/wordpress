## What's this?

This is a fast, simple and clean install for Wordpress with docker in few steps. 

## Customize

The Wordpress current version is the php7.4-apache but you can customize it if do you want in your `Dockerfile`.

## Requirements

- Docker

## Configuring

- Create your `.env` based in `.env.example` file
- Change the `docker-compose.yml` passwords that are exposed in this git repository

## Usage

### Building the image

If do you want to use my image `antonio24073/wordpress:4.5-apache` you can put it in the `.env` and jump this step.

```bash
make build
```

### Creating the volume folder

```bash
make run
make mkdir
make rm
```

### Running docker compose

```bash
make up
```

### Add production linux permissions

```bash
make perm
```

### Add developer linux permissions (optional)

If you need edit the files do it.

```bash
make perm_dev
```

### Install Wordpress if not installed

```bash
make install
```

## Access

### Running in Localhost

#### Ubuntu

Go to `/etc/hosts` and add `0.0.0.0 wordpress.local` or `0.0.0.0 your.url` 

To wordpress, access this url in the browser.

To PhpMyAdmin ou PgAdmin use `your.url:8081`


## Saving the image

Create a repository in the Docker Hub.

Be careful with the visibility of the repository, whether it is public or private. 

**If you do it without change the visibility in docker hub, it will be public.**

### Do the Docker Hub Login

```bash
make login
```

### Push

After build, you can push it:

```bash
make push
```
