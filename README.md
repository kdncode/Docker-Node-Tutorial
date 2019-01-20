# Node with Docker

Using Volumes And Nodemon.


## Usage

```
cd Docker-Node-Tutorial/

docker run -p 3001:3000 -v $(pwd):/app Docker-Node-Tutorial
```

# Step by step
## Installation

```
npm install

npm run start
```
Navigate to: [http://localhost:3000](http://localhost:3000)

## Build Docker Image
This will subsequently run through the 6 steps outlined within our Dockerfile and build our complete Docker image.
```
docker build -t Docker-Node-Tutorial .
```

## Run Docker Image
This will start up a Docker container based off our Docker-Node-Tutorial docker image and expose it on port 9000 on our machine. The -d flag specifies that we wish to run this in a detached mode which means that the docker container will run in the background on our host machine.
```
docker run -d -p 9000:3000 Docker-Node-Tutorial
```

## View running Docker Containers
This should show our Docker-Node-Tutorial container running and the ports that it’s listening to.
```
docker ps
```

## Automatically Picking up Changes
```
npm install --save nodemon

docker build -t Docker-Node-Tutorial-tutorial .

docker run -it -p 9001:3000 -v $(pwd):/app Docker-Node-Tutorial-tutorial
```
Navigate to: [http://localhost:9001](http://localhost:9001)



## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/) | 
[Credit](https://tutorialedge.net/docker/working-with-docker-nodejs/)