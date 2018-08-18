# dockertest

Pranavs-MacBook-Pro-10:dockertest Pranav$ docker image ls
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
dockertest          latest              efd124d3c96c        8 minutes ago       132MB
python              2.7-slim            40792d8a2d6d        2 weeks ago         120MB
Pranavs-MacBook-Pro-10:dockertest Pranav$ docker push pydhpe/dockertest
The push refers to repository [docker.io/pydhpe/dockertest]
An image does not exist locally with the tag: pydhpe/dockertest
Pranavs-MacBook-Pro-10:dockertest Pranav$ docker push pydhpe/latest
The push refers to repository [docker.io/pydhpe/latest]
An image does not exist locally with the tag: pydhpe/latest
Pranavs-MacBook-Pro-10:dockertest Pranav$ docker push pydhpe/dockertest
The push refers to repository [docker.io/pydhpe/dockertest]
An image does not exist locally with the tag: pydhpe/dockertest
Pranavs-MacBook-Pro-10:dockertest Pranav$ docker push latest
The push refers to repository [docker.io/library/latest]
An image does not exist locally with the tag: latest
Pranavs-MacBook-Pro-10:dockertest Pranav$ ls
Dockerfile       README.md        app.py           requirements.txt
Pranavs-MacBook-Pro-10:dockertest Pranav$ docker pull pydhpe/dockertest
Using default tag: latest
latest: Pulling from pydhpe/dockertest
be8881be8156: Already exists
44247e56d488: Already exists
9b1ccb116b10: Already exists
94c785725d8a: Already exists
0336a78e7125: Pull complete
56e8eb46fd01: Pull complete
b80671034550: Pull complete
Digest: sha256:d7654cdb2ac00150bf45f1bd29528ed6495bf32fcb1fb94afbf24f300dcfcca5
Status: Downloaded newer image for pydhpe/dockertest:latest
Pranavs-MacBook-Pro-10:dockertest Pranav$ docker image ls
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
dockertest          latest              efd124d3c96c        13 minutes ago      132MB
pydhpe/dockertest   latest              3b279c740c83        28 hours ago        132MB
python              2.7-slim            40792d8a2d6d        2 weeks ago         120MB
Pranavs-MacBook-Pro-10:dockertest Pranav$ docker run -p 4000:80 pydhpe/dockertest
 * Serving Flask app "app" (lazy loading)
 * Environment: production
   WARNING: Do not use the development server in a production environment.
   Use a production WSGI server instead.
 * Debug mode: off
 * Running on http://0.0.0.0:80/ (Press CTRL+C to quit)
172.17.0.1 - - [18/Aug/2018 23:52:27] "GET / HTTP/1.1" 200 -
172.17.0.1 - - [18/Aug/2018 23:52:27] "GET /favicon.ico HTTP/1.1" 404 -
