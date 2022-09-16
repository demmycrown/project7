## Documentation on Devops tooling website solution

1. Spin up NFS,WEB and DB servers

2. Create and attached volumes

`sudo yum -y update`

`rpcinfo -p | grep nfs`

`sudo yum install nfs-utils nfs4-acl-tools -y`

`sudo mkdir /var/www`

`sudo mount -t nfs -o rw,nosuid'172.31.88.149' :/mnt/apps /var/www`

`sudo systemctl restart nfs-server.service`

`sudo exportfs -arv`

`sudo yum install httpd -y`

`mysql -h  -u webacess -p tooling < tooling-db.sql`

	