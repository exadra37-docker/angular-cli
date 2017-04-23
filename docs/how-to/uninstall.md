# HOW TO UNINSTALL

In 3 simple steps you can uninstall it completely from your system.


## STEP 1

To remove stop and remove all running containers, from the folder where is the `docker-compose.yml` file just run:

```shell
sudo docker-compose down
```


## STEP 2

Now we need to remove also the Docker Image we have created by running the command:

```shell
sudo docker image rm node-zsh
```


## STEP 3

Delete the folder where you have cloned it.
