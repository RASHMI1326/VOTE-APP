# VOTE-APP
Project
-------
https://github.com/rashmi1326devops/Voting-application.git
git@github.com:rashmi1326devops/Voting-application.git
create three images
create redis container
 docker run -d --name redis -h redis redis
               (imagename)     (hostname)  (image)

redis - memory cache msgs
check docker ps
create Postgres container
 docker run -d --name postgres -h postgres -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=postgres postgres
check container - 2 containers are running
creating link to Vote app from redis
docker run -d -p 1000:80 --link redis:redis vote 
                                      (Provider name ) (image name)
check using insta ip address
connect worker application with two databases
 docker run -d --link redis:redis --link postgres:db worker

create link postgres db to result app
 docker run -d -p 1001:80 --link postgres:db result
