https://linuxhint.com/cleanup-docker/

docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
docker rmi $(docker images -f "dangling=true" -q)

#BEST BEST HERE
#clear it all
docker system prune -a --volumes

memory hogs alternative
brew install ncdu
sudo du -shc /path/to/place/*
