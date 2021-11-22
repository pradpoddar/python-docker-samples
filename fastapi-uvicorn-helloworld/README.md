## This is a hello-world sample docker image using fastapi on uvicorn.


After you clone this code, run "docker build" to build a docker image out of it from the root location of the cloned code directory.
```docker
$ docker build -t fastapi-uvicorn:localtest .
.
.
.
=> => naming to docker.io/library/fastapi-uvicorn:localtest
```


The above "docker build" command creates a image called fastapi-uvicorn:localtest in your local system. You can verify that by running "docker images" as below, and it should return the newly built docker image.
```docker
$ docker images
REPOSITORY        TAG         IMAGE ID       CREATED          SIZE
fastapi-uvicorn   localtest   631a864f8f4a   2 minutes ago    54.2MB
```


Now, we can run this image as a container in local system using "docker run" command. You can learn about various "docker run" options from https://docs.docker.com/engine/reference/run/.
```docker
$ docker run -it --rm -p 80:80 fastapi-uvicorn:localtest
INFO:     Started server process [1]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
INFO:     Uvicorn running on http://0.0.0.0:80 (Press CTRL+C to quit)
```


Now you can see the application actually running in your local system going to http://0.0.0.0:80 which will open a simple web page saying "{"Hello":"World"}". Yes, you can also go to http://0.0.0.0:80/docs to see the Swagger UI.

Thank you.
