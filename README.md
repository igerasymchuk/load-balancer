# proxyTest
Load Balancing Applications with HAProxy and Docker

docker build -t awesome
docker swarm init
docker stack deploy --compose-file=docker-compose.yml prod

docker service ls
docker service scale prod_awesome=2

docker service update --image awesome:v2 prod_awesome

docker swarm leave --force