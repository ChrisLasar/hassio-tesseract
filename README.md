# hassio-tesseract
Docker container for a hass.io/ResinOS environment to enhance scanned pages with OCR

## Build and Test locally
```bash
sudo docker build -t tesseract .
sudo docker run --name testeract --rm -i tesseract bash &
sudo docker exec -it testeract bash

sudo docker kill <container id> # See sudo docker ps to get the container id
```

## Input and Output of Examples
```bash
sudo docker cp testeract:/testres.pdf testres.pdf
```

## Sources and Further Information
* Installation of tesseract into an Alpine Linux docker container is inspired by https://github.com/gnkm/docker-alpine-tesseract-jpn/blob/master/Dockerfile
* see [Hass.io's Local Add-On Testing page](https://home-assistant.io/developers/hassio/addon_testing/) for further information on how to test containers on another archtecture before deploying it
* see [`docker exec`](https://docs.docker.com/engine/reference/commandline/exec) description on how to run and modify a docker container with a bash
