  # Stop all containers
  docker stop $(docker ps -aq)

  # Remove all containers
  docker rm $(docker ps -aq)

  # Remove all images
  docker rmi $(docker images -aq)

  # Remove all volumes (⚠️ deletes all data)
  docker volume rm $(docker volume ls -q)

  # Remove all networks (except defaults)
  docker network prune -f
