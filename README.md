                                  LAMP stack built with Docker Compose and kubernetes


For Docker Compose:-

Enviroments:-
. Mysql5.7
. phpmyadmin
. php:7.1.2-apache

Installation:-
Clone this repository on your local computer. 


1. git clone https://github.com/sadhaura/docker_lamp_kubernetes.git

2. cd docker_lamp_kubernetes/

3. docker-compose up -d

Your LAMP stack is now ready!! You can access it via http://localhost:8002.

You can access phpmyadmin via http://localhost:8003 with username root/user1 and password test1


For kubernetes:-

we can use any kubernetes enviroments like EKS,GKE,Minikube etc.In this example we are using google cloud 
Requirements:-

1. Google cloud kubernetes cluster up and running.

clone the repository 
git clone https://github.com/sadhaura/docker_lamp_kubernetes.git

cd docker_lamp_kubernetes/kubernetes

run the below command :-

kubectl create -f apache.yml,configmap.yml,secret.yml,mysql.yml,volume.yml

your kubernetes deployments,pods,service will be up and running with persistent volume for database.

You can check access your website with EXTERNAL IP of kubernetes service(my-php7-server).







