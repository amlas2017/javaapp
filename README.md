Ce projet permet de créer un contenair docker à partir d'un dockerfile , copier un jar dedans avant de l'executer.

[vagrant@server00 testgitlab]$ tree
.
├── javaapp
│   ├── Dockerfile
│   └── Helloworld.java
└── README.md

[vagrant@server00 javaapp]$ sudo docker build -t javaapp:v1 .

//  docker build -t ImageName:tagName /location/of/Dockerfile
 si pwd = /location/of/Dockerfile , on met "." , cela signifie que Dockerfile est dans le dossier courant (pwd)

[vagrant@server00 javaapp]$ sudo docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
javaapp             v1                  51b1de32ffaa        6 minutes ago       625 MB
docker.io/openjdk   8                   b8d3f94869bb        4 weeks ago         625 MB


[vagrant@server00 javaapp]$ sudo docker run -it --name maVersion javaapp:v1

[vagrant@server00 javaapp]$ sudo docker run -it --name maVersion3 javaapp:v2
