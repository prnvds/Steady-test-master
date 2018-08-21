
===========================================
Python app on a Docker container staged in AWS
===========================================
1. Fork this repo into your own github account
2. Get a simple api application running in the language of your choice. A sample flask application is
   provided in app.py. Feel free to use that if you want. It needs to listen on a single endpoint and return
   some text like "Hello world" on a GET
3. Get the api service running in a container using a Dockerfile.
   The Dockerfile needs to be added to the root directory of the repo.
4. Configure a CI tool to build the dockerfile and push it to a public dockerhub repo.
5. Using the free tier of your favorite cloud system, launch a means to run a container.
   In aws this could be eks,fargate, ecs, or ec2. Include in this repo any infrastructure as code
   toolingi/config you use.
6. Configure the same CI tool to deploy your container on the infrastructure you created when there is a
   change to the repo
7. Provide a url to the api application. We will test the pipeline by making a code change and watching
   our change show up on the url provided

===========================================
Approach
===========================================
1) created a simple python app ( app.py )
2) verified docker and github are synced with my local machine and with each other.
3) configured a Dockerfile and requirements.txt ( same repository as the app)
4) build and ran the docker image ( browse : http://192.168.99.100:4000)

   * Running on http://0.0.0.0:80/ (Press CTRL+C to quit)
   172.17.0.1 - - [18/Aug/2018 23:52:27] "GET / HTTP/1.1" 200 -
   172.17.0.1 - - [18/Aug/2018 23:52:27] "GET /favicon.ico HTTP/1.1" 404 -

5) pushed the docker image to dockerhub
6) added, commited and pushed the repo to Github
7) verified the app if it runs locally as well as from container image
8) shipped the docker container to AWS EC2 using cloudformation.

docker-machine ip : 192.168.99.100
