# HOW TO USE

This are some of the ways we can use this image, but is not an exhaustive list of commands we can run against it.

You may want to the [Hello App](https://gitlab.com/exadra37-docker-images/angular-cli/blob/master/docs/examples/hello-app.md) example.

All commands we will run from this examples assumes that:

* We are inside the `src` directory of this repository, where the `docker-compose.yml` lives, that following the Install example would be `~/Developer/Acme/Angular2/HelloApp/docker/angular-cli/src`.
* Docker is installed in your system in a recent version.
* Docker Compose is installed and supports at least version 2 for parsing `docker-compose.yml` files.


## Build the Angular CLI local Docker Image

This step is optionally, because the first time you execute a `sudo docker-compose run` command it will build the image.

When building the image we can customize:

* The Angular CLI version we want to use.
* The Node port we want to expose from inside the Docker Container.
* The Image Name.
* The Image Tag.

Just open the `src/.env` file and adjust as per need.

```bash
sudo docker-compose build
```

## Run the Angular CLI Container

This is the container we will use most of the time in our development workflow.


#### Keeps the Container after you exit it.

```bash
sudo docker-compose run angular-cli
```

#### Removes the Container after you exit it.

```bash
sudo docker-compose run --rm angular-cli
```

#### Run the Container with Ports Mapping Enabled

Using the flag `--service-ports` we tell Docker Compose to start the container and map the defined ports in the docker compose file.

Useful if we want to use run our App in the browser from inside the container `ng serve --host 0.0.0.0` and then we can access it in http://localhost:4200, where `4200` must match the port number defined in the `.env` file in `HOST_PORT` Argument.

```bash
sudo docker-compose run --rm --service-ports angular-cli
```


## Run Container with Node CLI

This will give you access to the `node` CLI shell inside the Docker Container.

```bash
sudo docker-compose run node-cli
```

## Run Container as Root User

In case you need to access the Container as the Root User.

```bash
sudo docker-compose run root-user
```


[HOME](https://gitlab.com/exadra37-docker-images/angular-cli)
