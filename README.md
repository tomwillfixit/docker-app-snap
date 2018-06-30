# Using docker-app in a snap

One of the most exciting announcements at DockerCon 2018 was an experimental tool called "docker-app". It was demoed during the Day 1 Keynote and can be watched [here](https://dockercon2018.hubs.vidyard.com/watch/ExN8mYJWm93MfUREaSzajh).

More details on docker-app can be found in this [post](https://blog.docker.com/2018/06/compose-easier-to-use-with-application-packages/) by Gareth Rushgrove 

If you are a linux user you can install docker-app as a snap and take it for a spin.

This snap isn't available in the snapcraft store yet.  I had to use the --classic mode in order for the docker-app snap to be able to access docker installed outside of snap.  I'm new to snap so if there is an easier way to achieve this then I'm happy to listen.

## Build

Visit snapcraft.io and download the tools needed to build a snap.

```
cd build
snapbuild cleanbuild
snap install docker-app_v0.3.0_amd64.snap --classic --dangerous
snap list
```

## Install

If you are feeling adventurous you can install the pre-built .snap application in this directory. Just clone this repo and run :

```
snap install docker-app_v0.3.0_amd64.snap --classic --dangerous
```

## Remove

To remove the docker-app snap run :

```
snap remove docker-app
```

## docker-app

Try running a few commands after installing the snap :
```
docker-app
docker-app version
docker-app ls

```

There are some examples available in the docker-app github [repo](https://github.com/docker/app/tree/master/examples).

Enjoy.
