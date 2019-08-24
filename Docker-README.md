http://localhost:8080/spring-docker/hello

with docker for windows
http://10.0.75.1:8080/spring-docker/hello

docker inspect --format '{{ .NetworkSettings.IPAddress }}' 

016973021151.dkr.ecr.eu-central-1.amazonaws.com/ungerw/codebuild:springboot


docker build -f src/main/docker/Dockerfile -t $TAG_NAME .
docker build -f src/main/docker/Dockerfile -t 016973021151.dkr.ecr.eu-central-1.amazonaws.com/ungerw/codebuild:springboot .
  
 
docker run -d -p 8080:8080 016973021151.dkr.ecr.eu-central-1.amazonaws.com/ungerw/codebuild/sprinboot:latest


$(aws ecr get-login --no-include-email --region eu-central-1)

docker push 016973021151.dkr.ecr.eu-central-1.amazonaws.com/ungerw/codebuild:springboot



  
