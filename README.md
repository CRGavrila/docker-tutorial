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



