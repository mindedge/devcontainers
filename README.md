To Build container :
docker build  -t mindedge/php82  -f ./docker/php82/Dockerfile .
docker build  -t mindedge/php81  -f ./docker/php81/Dockerfile .


to push container to docker hub :

 docker push mindedge/php82:latest
 docker push mindedge/php81:latest
