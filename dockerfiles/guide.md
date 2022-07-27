1. build tfw
2. connect enviroments (do they also auto resatart?)
3. send pipeline files

test build on azure cloud

1 machine + 1 db

figure out what needs to be done on the devops

1. rebuild tf - make it work then make it solid with alban.
   a- make it work status - {{CHAOS - leave it for now handle the rest}}
   2.build the dockerfile
2. build the ci cd pipeline- use the vids.
3. try to see if you can build a pipeline for terraform.

docker run -d --name measurements -p 5432:5432 -e 'POSTGRES_PASSWORD=p@ssw0rd42' postgres

docker build -t weightapp/version:1.0.0 .

docker run 8ef6abc8c62e

docker tag local-image:tagname new-repo:tagname

questions:

docker compose

still gets confused around:
RUN, CMD and entrypoint

build a container
pull a specific version from hub

delete: docker rmi -f <image_id>

docker rm $(docker ps --filter status=exited -q)
docker rm $(docker ps -a -q) //research this
rmi - deletes image
rm deletes container

docker rmi($(docker images -q ))
tag -study

<!-- docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG] -->

docker run -it -d alpine
docker commit 813d8d499101 johnmogi/alpine:1.0.0

the tag is run on the commit

alpine
create
docker container create -i -t --name mycontainer alpine
docker tag d7b61c403747 ver:1.0.0

tag 1.0.0

commit - save

exec

<!-- docker exec <container-id> <tool>
docker run --name weightapp --rm -i -t 65b4080c87c2 sh -->

docker exec -it a127649667c9 sh

docker save
load

docker build -t <name>:1.0.0 .
docker build -t <name>:1.0.0 --build-arg NAME="john" .

docker build -t weightapp:1.0.0 .

docker push new-repo:tagname
docker push johnmogi/weightapp:1.0.0

docker tag weightapp:1.0.0 johnmogi/weightapp:1.0.0
docker push new-repo:weightapp

docker run weightapp:1.0.0-p 8080:8080
docker run weightapp:1.0.0 -p 8080 

docker start `docker ps -q -l`
