Ce projet permet de créer un contenair docker à partir d'un dockerfile , copier un jar dedans avant de l'executer.

[vagrant@server00 testgitlab]$ tree
.
├── javaapp
│   ├── Dockerfile
│   └── Helloworld.java
└── README.md

[vagrant@server00 javaapp]$ sudo docker build -t javaapp:v1 .

