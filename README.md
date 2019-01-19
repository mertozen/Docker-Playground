# Docker-Playground
- docker run -p 27017:27017 -d mongo
- docker logs -f 7288df18a05d
- docker image inspect mongo
- docker network create elknetwork
- docker run -d --name kibana --net elknetwork -p5601:5601 kibana:6.5.4
- docker run -d --name elasticsearch --net elknetwork -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" elasticsearch:6.5.4
- docker run -d --name postgres -p 5432:5432 -e POSTGRES_PASSWORD=1 postgres
- docker run --name guru-mysql -e MYSQL_ALLOW_EMPTY_PASSWORD=yes -v /usr/server/mysql -p 3306:3306 -d mysql
- docker run -d --hostname rabbit --name rabbitmq -p 8080:15672 rabbitmq:3-management
