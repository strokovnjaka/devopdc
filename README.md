# Excercises in style: app stack in docker images

## For essa-vm-07.lrk.si prerequisites

Install docker, via sh script:
```
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh ./get-docker.sh
```

## Setup

1. start `setup` profile with 
```
sudo docker compose --profile setup up
```
2. init db with 
```
sudo docker exec dc_mongo_db mongoimport --db shroomate --collection Species --mode upsert --upsertFields id --jsonArray --file /db_species.json
sudo docker exec dc_mongo_db mongoimport --db shroomate --collection Users --mode upsert --upsertFields id --jsonArray --file /db_users.json
```
3. check certbot successfull, kill `nginx_cert` with `CTRL-c`
4. optionally cleanup with 
```
sudo docker container prune
```

## Running

Start `run` profile with 
```
sudo docker compose --profile run up
```
