# Docker-Operation

# Steps 1:
sudo apt-get update

![image](https://user-images.githubusercontent.com/71307854/229224568-ec22cfa7-9c96-49dd-b9ce-53ade1e8e5f6.png)

To install Docker 
 sudo apt install docker.io
 
 ![image](https://user-images.githubusercontent.com/71307854/229224701-f39964c0-2c85-4234-9404-e8c05b8e3fdc.png)


To see docker version 
sudo docker --version

![image](https://user-images.githubusercontent.com/71307854/229224851-76136aa1-5051-440a-ba39-d00d800f2191.png)

To pull image  Ubuntu
 sudo docker pull ubuntu
 
 ![image](https://user-images.githubusercontent.com/71307854/229224997-50aa82e9-16a3-4be1-83ae-eb26bc822a95.png)
 To See images 
  sudo docker images

![image](https://user-images.githubusercontent.com/71307854/229225092-96332e0c-9314-4dfa-8245-56c122ff572d.png)

sudo docker ps

![image](https://user-images.githubusercontent.com/71307854/229225136-994f44be-1473-4f4e-82f5-a03e2dcd0ec7.png)
To enter the container
 sudo docker exec -it 93c4cb120b76 bash
 
 ![image](https://user-images.githubusercontent.com/71307854/229225208-9ee35c91-1086-4e1b-9136-e85d366740a8.png)

sudo docker ps

![image](https://user-images.githubusercontent.com/71307854/229225278-7e0e1d70-5dee-4139-87da-bddb38d56291.png)

To remove container
 sudo docker rm <CI>
 
 ![image](https://user-images.githubusercontent.com/71307854/229225392-4e0064a5-f382-4e2a-9282-3c89a562d364.png)
 
 ![image](https://user-images.githubusercontent.com/71307854/229225481-24f6ce8f-d86c-4f73-9e1c-01ce97b42438.png)

After Deleting all conatiners
 sudo docker run -it -d ubuntu
 
![image](https://user-images.githubusercontent.com/71307854/229225592-2ff27e3b-c610-49b9-bb83-66d0ba67c5e9.png)

then enter the conatiner

![image](https://user-images.githubusercontent.com/71307854/229225645-b451721e-985a-402e-9362-22ff764d0a19.png)

to save images with addition in container 

![image](https://user-images.githubusercontent.com/71307854/229225999-8bf65292-71b3-47d1-8fca-5cbbc42ec047.png)

To remove all container at one time 

 sudo docker rm -f $(sudo docker ps -a -q)

![image](https://user-images.githubusercontent.com/71307854/229226435-8a4dfbc4-b4d9-475d-8a7c-8eea76670866.png)

To install apache2

 sudo docker exec -it <CI>  bash

apt-get install apache2

![image](https://user-images.githubusercontent.com/71307854/229226894-89521268-af91-4102-988d-896b9d9f20ff.png)

 After
 
![image](https://user-images.githubusercontent.com/71307854/229227203-aceb4982-7d9a-48d6-96b2-a07f79cdf956.png)


To push it into dockerhub 
To login 
sudo docker login

![image](https://user-images.githubusercontent.com/71307854/229227422-d08b385a-1e83-42ad-9835-2e2890d7f1ba.png)

After Login Successfull login message will be displayed
 sudo docker push nikhil3389/apache

![image](https://user-images.githubusercontent.com/71307854/229227519-0322455a-8559-4774-afb9-9620d7fc3ba9.png)

Then open your DockerHub

![image](https://user-images.githubusercontent.com/71307854/229227718-c0ef00e9-73ba-4a22-aa3d-2028521e97fb.png)

# Step 2: DockerFile

Create new directory

mkdir <Dockerfile>

cd <Dockerfile>

Create new Dockerfile into the create directory

nano <Dockerfile>

FROM ubuntu

RUN apt-get update

RUN apt-get -y install apache2

ADD . /var/www/html

ENTRYPOINT apachectl -D FOREGROUND

ENV name Nikhil

— Save the file Control + x, then Y, then Enter



Create new html file
>>nano 1.html

>><html>

>><head><title>Hello world</title></head>


>><body>

>><h1>Welcome to the world of Devops</h1>

>></body>

>></html>

— Save the file Control + x, then Y, then Enter

![image](https://user-images.githubusercontent.com/71307854/229228040-e90088b6-d845-43d6-a246-57f0979c4235.png)

Build new dockerfile

sudo docker build . -t new_dockerfile

![image](https://user-images.githubusercontent.com/71307854/229228102-b5b94660-141f-4093-be95-f09209d828d8.png)

Then run 
sudo docker images

![image](https://user-images.githubusercontent.com/71307854/229228210-a39ca318-d5c2-455f-a9ac-f82d437bac8b.png)






