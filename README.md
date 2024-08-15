Домашнее задание к занятию 4 «Оркестрация группой Docker контейнеров на примере Docker Compose»

Задача 1

https://hub.docker.com/repository/docker/eugene513/custom-nginx/tags

Задача 2

![alt text](Task2.png)

Задача 3

![alt text](Task3_1.png)

Ctrl+C передает SIGINT

![alt text](Task3_2.png)


![alt text](Task3_3.png)


Нарушено port mapping, т.к контейнер был запущен командой:

docker run --name TEV-custom-nginx-t2 -d -p 127.0.0.1:8080:80 eugene513/custom-nginx:1.0.0


docker stop custom-nginx-t2

systemctl stop docker

Изменения в файлах:

hostconfig.json(PortBindings":{"81/tcp":[{"HostIp":"127.0.0.1","HostPort":"8080"}]})

config.v2.json(ExposedPorts":{"81/tcp":{}})

systemctl start docker

![alt text](Task3_4.png)

docker rm -f custom-nginx-t2

-f, --force		Force the removal of a running container (uses SIGKILL)

![alt text](Task3_5.png)



