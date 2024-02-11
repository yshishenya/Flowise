sudo docker compose down
sudo docker rmi $(sudo docker images -f "dangling=true" -q) -f
sudo docker image prune -f
sudo docker container prune -f
sudo docker rmi flowiseai/flowise
sudo docker compose up -d

Более простая версия:

sudo docker compose stop
sudo docker compose rm
sudo docker pull flowiseai/flowise
sudo docker compose up -d
