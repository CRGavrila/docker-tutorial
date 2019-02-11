development -> testing -> deployment

flow:

github rep:
feature branch -> pull request master -> travis CI -> AWS CLOUD

// should remove node_modules or add a Dockerignore file
docker build -f Dockerfile.dev .
docker run -p 3000:3000 <docker_id>

We must add reference to folders with volumes like:
-v $(pwd):/app
-v /app/node_modules

in windows must have in .env : CHOKIDAR_USEPOLLING=true , render new savings
docker run -p 3000:3000 -v /app/node_modules -v ${pwd}:/app <docker_id>

