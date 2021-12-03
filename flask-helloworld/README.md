## This is a hello-world sample docker image using flask.


After you clone this code, run "docker build" to build a docker image out of it from the root location of the cloned code directory.
```docker
$ docker build -t flask-helloworld:localtest .
.
.
.
=> => naming to docker.io/library/flask-helloworld:localtest 
```


The above "docker build" command creates a image called flask-helloworld:localtest in your local system. You can verify that by running "docker images" as below, and it should return the newly built docker image.
```docker
$ docker images
REPOSITORY         TAG         IMAGE ID       CREATED          SIZE
flask-helloworld   localtest   ccfbeadf2518   2 minutes ago    55.1MB
```


Now, we can run this image as a container in local system using "docker run" command. You can learn about various "docker run" options from https://docs.docker.com/engine/reference/run/.
```docker
$ docker run -it --rm -p 80:80 flask-helloworld:localtest
 * Serving Flask app 'main' (lazy loading)
 * Environment: development
 * Debug mode: on
 * Running on all addresses.
   WARNING: This is a development server. Do not use it in a production deployment.
 * Running on http://172.17.0.2:80/ (Press CTRL+C to quit)
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 844-983-912
172.17.0.1 - - [03/Dec/2021 05:38:08] "GET / HTTP/1.1" 200 -
```


Now you can see the application actually running in your local system going to http://localhost:80/.


Thank you.
