# docker-tutorial

Run first time: docker run hello-world
    Because the image hello-world doesn't exist it will download it and execut it
Run second time: docker run hello-world
    Will only execut the image because the image is stored in the cache of computer

Run: docker run busybox echo hi there and it      will install to your locally machine and      execute the command echo
Run: docker run busybox ls
    wll show the container files

docker run hello-world echo or docker run hello-world ls will not work beacuse these cmds dowsn't exist in this container

when run: docker run busybox ping google.com and open another cmd propmts if you check docker ps will see the image running
if you run docker run busybox echo hello, etc will show that this image will run and after comand is done it will deleted itself


run:
c_r_g@DESKTOP-IC84403 MINGW64 /d/tutorials/docker-tutorial (master)
$ docker create hello-world
00f9ac73bae181a50276ff85be8584c8b0f76db62afe0bcf3e4f70e2da581820

will return the id of the container

run:
docker start -a 00f9ac73bae181a50276ff85be8584c8b0f76db62afe0bcf3e4f70e2da581820

-a is a watch the output and print it


docker start -a container-id-name

docker system prune - will delete couple of things and all containers


Log outputs:
docker create busybox echo hy there
docker start 8100c6b5ab28efe4545e5e59619ef55169d8bd6650ccb88262181ed288ce4279
docker logs --details 8100c6b5ab28efe4545e5e59619ef55169d8bd6650ccb88262181ed288ce4279

execute commands in running containers
docker exec -it <container id> <command>

Redis:

docker run redis
another terminal:
    docker ps
    docker exec -it 42217609693e redis-cli
    set myvalue 5
    get myvalue

    >>
    docker exec -it 42217609693e sh
    will go to linux container and to exit: ctrl+d or ctrl+c

    sh, bash, powershell, zsh: command processor

    Building a dockerfile:

    In redis-image folder is the workaround !!!

    Create file: Dockerfile
    Add the code
    and build the image: docker build .
    and run: docker run 97f231db5ced

    added a second RUN cmd and docker uses a cache and will not download previous packages... ONLY the order of RUN cmds will not change!!!!



