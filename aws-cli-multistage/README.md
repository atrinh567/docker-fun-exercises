Same as `aws-cli` - but with multistage build

docker build aws-cli -t awscli:0.0
docker run -d awscli:0.0
docker exec -it <container_id> /bin/bash