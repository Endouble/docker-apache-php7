# docker-apache-php7

*This repo is now deprecated in favour of [tap_docker_images](https://github.com/Endouble/tap_docker_images)*

To build the image you can run:

    docker build -t endouble/taf-apache-php7 .

If you're rebuilding an existing image you need to remove it first: 

    docker rmi -f <uuid>

and stop all containers using it:

    docker ps # find containers using the image
    docker rm <uuid> # remove them one-by-one

To get the `uuid` for the image:

    docker images

To get the `uuid` of a container:

    docker ps -a

To tag a newly-build-image:

    docker tag endouble/taf-apache-php7 endouble/taf-apache-php7:<tag_version>

E.g.:

    docker tag endouble/taf-apache-php7 endouble/taf-apache-php7:0.0.1

To push to docker hub (assuming you have access):


    docker push endouble/taf-apache-php7

You can see if image was successfully pushed at: https://hub.docker.com/r/endouble/taf-apache-php7/
