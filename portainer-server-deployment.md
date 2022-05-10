### Docker
1. Create a new volume
```
docker volume create portainer_data
```
2. Run portainer and expose port 9001
```
docker container run -d -p 9001:9001 --name portainer_agent --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v /var/lib/docker/volumes:/var/lib/docker/volumes portainer/agent
```

### Docker Swarm
1. Download script yml
```
curl -L https://downloads.portainer.io/portainer-agent-stack.yml -o portainer-agent-stack.yml
```
2. Run portainer and expose port 9000 and 8000
```
docker stack deploy -c portainer-agent-stack.yml portainer
```

Referrence: https://docs.portainer.io/v/ce-2.11/start/install/server/swarm/linux
