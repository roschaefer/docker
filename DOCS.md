* 1 Create a folder named *code* that will work as a work directory.
* 2 Put your source file in the *code* directory
* 3 Start the containers using:
    docker-compose -f docker-compose.yml  up --build
* 4 Access to the services through http://127.0.0.1:5000 (port configurable in the docker-compose.yml)
* 5 (opt) For an initial setup you'll need to init MongoDB, configurations, etc (see communecter install guide for more detail), an easy to use script is provided through install.sh
$ # Enter your container through `docker exec` (you can use `docker ps` to see which containers are running
$ docker ps
CONTAINER ID        IMAGE                     [...] NAMES
279479507ecb        pixelhumaindocker_front   [...] pixelhumaindocker_front_1
e5532c34570e        mongo                     [...] pixelhumaindocker_mongo_1

$ docker exec -ti pixelhumaindocker_front_1 /bin/bash
$ # Then execute the install script
$ /tmp/install.sh