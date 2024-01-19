# Notes

## For essa-vm-07.lrk.si prerequisites

Install docker, via sh script:
  - `curl -fsSL https://get.docker.com -o get-docker.sh`
  - `sudo sh ./get-docker.sh`


## Running

1. start all but certbot `sudo docker compose up` + detach

2. run certbot with `certbot/conf/live` dir cleaned up: `sudo rm -rf certbot/conf/live && sudo docker compose run certbot`

3. restart nginx `sudo docker restart dc_nginx`