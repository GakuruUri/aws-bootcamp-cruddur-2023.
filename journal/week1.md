# Week 1 — App Containerization
Launched an EC2 instance with Docker installed.

![steps installing docker on EC2](https://user-images.githubusercontent.com/27725033/220609115-3887b443-5d19-408a-a8f3-477959c43e0f.png)

 ![Docker Install EC2 CMD](https://user-images.githubusercontent.com/27725033/220609301-10587069-41d0-47f8-b560-90e48ac99455.png)

 Successfully run Docker on an EC2 Instance!

[Docker working Success on EC2](https://user-images.githubusercontent.com/27725033/220609537-26cab317-45a3-4858-9574-b1667872ff8b.png)

Successfull Installation of Docker on Local Env

![Successfuly installed Docker Ubuntu Desktop](https://user-images.githubusercontent.com/27725033/220609617-ad9bfeed-5cf7-4ab7-8a9b-675e65ee951a.png)

KMV errors on Ubuntu desktop!

[Ubuntu KMV error](https://user-images.githubusercontent.com/27725033/220609837-c4ba954b-fa92-4358-86e5-927b338f8a35.png)

Successfully running a docker image on Ubuntu 22.04 Laptop!

[Docker Build On Local Machine](https://user-images.githubusercontent.com/27725033/220610006-5aadd18d-9698-4d0f-bd78-f8a4f0897226.png)

![Docker research](https://user-images.githubusercontent.com/27725033/220610119-3e0abd2c-5f99-4c28-89c7-66fe0421c110.png)!

[Research on docker errors](https://user-images.githubusercontent.com/27725033/220610191-342641b5-666c-49fa-962f-3a24e79f7e4e.png)

https://stackoverflow.com/questions/24993704/docker-error-cannot-start-container-port-has-already-been-allocated

Managed to create a multi-stage dockerfile build.
````
To write a multi-stage Dockerfile, you need to use multiple FROM statements, each with a different base image. You can name each stage using AS keyword, and copy artifacts from one stage to another using COPY --from=stage_name command².

For example, you can create a multi-stage Dockerfile for a React application that uses Nginx to serve the app¹:

```
# Stage 1: Build React app
FROM node:14-alpine as builder
WORKDIR /app
COPY package.json yarn.lock ./
RUN yarn install
COPY . .
RUN yarn build

# Stage 2: Serve app with Nginx
FROM nginx:alpine
COPY --from=builder /app/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
```
````
DockerFile Multi-stage build and Docker images Best practise.

https://www.howtogeek.com/devops/what-are-multi-stage-docker-builds

https://www.padok.fr/en/blog/docker-image-multi-staging

https://www.toolsqa.com/docker/multi-stage-builds-in-docker

https://devopspilot.com/content/docker/tutorials/Dockerfile/03-create-multi-stage-dockerfile.html

https://docs.docker.com/build/building/multi-stage

https://docs.docker.com/develop/develop-images/dockerfile_best-practice



Worked successfully on notifications button as per instructions without problems!

[notifications reply 200](https://user-images.githubusercontent.com/27725033/220610393-a61b7cb6-321c-4fbc-905a-cd336cba6b15.png)!

[Notifications Working !](https://user-images.githubusercontent.com/27725033/220610430-2e318a80-75e8-4c3b-8dd6-0d479a80f48a.png)!

[Rinning the F_end and B_End](https://user-images.githubusercontent.com/27725033/220610588-cf6391d7-47b3-4223-94dc-ecfe902a03a3.png)

Git Push error reslolution!

[Git push wasn't working](https://user-images.githubusercontent.com/27725033/220610694-645ab25d-ab8b-45e1-a5b5-7ce80bf14a6f.png)

![Free port](https://user-images.githubusercontent.com/27725033/220610733-182bcc5c-1783-4a0c-97aa-d508e3fa3e57.png)

![Finally freed port](https://user-images.githubusercontent.com/27725033/220610814-91c60647-279c-4cd2-9239-dc554222f9ca.png)



PostgreSQL and DynamoDB![PostgreSQL](https://user-images.githubusercontent.com/27725033/220610542-09118196-c43a-4e6b-a0cd-b718c62c5990.png)


