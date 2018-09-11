#run mysql db:
docker run \
--detach \
--name=test-mysql \
--env="MYSQL_ROOT_PASSWORD=mypassword" \
--publish 3306:3306 \
--volume=/home/codetime/storage/docker/mysql-datadir:/var/lib/mysql \
mysql:5.7.22

#run mysql cli:
mysql -uroot -pmypassword -h 172.17.0.2 -P 3306


