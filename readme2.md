# First need to create container image, download the redis image and start the application.
docker-compose up -d

# When completed, use the docker images command to see the created images. Three images are downloaded or created. The azure-vote-front image contains the front-end application and uses the nginx-flask image as a base. The redis image is used to start a Redis instance.

$ docker images

REPOSITORY                                     TAG                 IMAGE ID            CREATED             SIZE
mcr.microsoft.com/azuredocs/azure-vote-front   v1                  84b41c268ad9        9 seconds ago       944MB
mcr.microsoft.com/oss/bitnami/redis            6.0.8               3a54a920bb6c        2 days ago          103MB
tiangolo/uwsgi-nginx-flask                     python3.6           a16ce562e863        6 weeks ago         944MB

# Run the docker ps command to see the running containers.

$ docker ps

CONTAINER ID        IMAGE                                             COMMAND                  CREATED             STATUS              PORTS                           NAMES
d10e5244f237        mcr.microsoft.com/azuredocs/azure-vote-front:v1   "/entrypoint.sh /sta…"   3 minutes ago       Up 3 minutes        443/tcp, 0.0.0.0:8080->80/tcp   azure-vote-front
21574cb38c1f        mcr.microsoft.com/oss/bitnami/redis:6.0.8         "/opt/bitnami/script…"   3 minutes ago       Up 3 minutes        0.0.0.0:6379->6379/tcp          azure-vote-back

# To see your running application, navigate to http://localhost:8080 in a local web browser. The sample application loads, as shown in the following example.
![Annotation 2022-12-16 125403](https://user-images.githubusercontent.com/102173014/208045406-65ee97ad-49f7-461d-8d70-f0243c213a05.png)

![Capture](https://user-images.githubusercontent.com/102173014/208044979-57e11888-b93b-4f5e-86de-3b5537492d8f.PNG)


(https://github.com/Naradsingh/Voting-App/files/10243549/Kubernetes.on.Azure.tutorial.-.Prepare.an.application.-.Azure.Kubernetes.Service._.Microsoft.Learn.pdf)
