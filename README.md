# React + TypeScript + Vite


#Білдимо та створюємо новий образ (front + back)
```

docker images

#Створення image
docker build -t transfer-front .

#Перед цим залогінитись у hub.docker.com
docker login

#Створення тега
#tag - це назва репозиторія на hub.docker.com
docker tag transfer-front:latest avalentyn/transfer-front:latest

docker images

#Запушити image на hub.docker.com
docker push avalentyn/transfer-front:latest

#Видалити image
docker rmi avalentyn/transfer-front:latest
docker rmi transfer-front

docker run -d --restart=always --name transfer-front-container -p 5234:80 avalentyn/transfer-front:latest
docker run -d --restart=always --name transfer-front-container -p 5233:80 transfer-front:latest          

```