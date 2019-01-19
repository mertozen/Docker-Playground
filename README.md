# Docker-Playground
- docker run -p 27017:27017 -d mongo
- docker logs -f 7288df18a05d
- docker image inspect mongo
- docker network create elknetwork
- docker run -d --name kibana --net elknetwork -p5601:5601 kibana:6.5.4
- docker run -d --name elasticsearch --net elknetwork -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" elasticsearch:6.5.4
