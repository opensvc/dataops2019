# Binlogic DataOps2019 - Barcelona - 20/21 June

This repository tracks files used during "Postgres LXC & Docker Containerized deployment with OpenSVC" techtalk

## Part 1 : LXC

Youtube video : https://www.youtube.com/watch?v=OC7VCpb5nKI

- Form OpenSVC cluster
- Create Postgres in LXC template through cli
- Provision & test service 
- Failover service


### opensvc.template.lxc.pg.conf

OpenSVC service template to deploy Postgres through LXC container

### opensvc-postgresql.yaml

Ansible playbook used in previous template, in LXC container post provision hook, to install and configure Postgres database

## Part 2 : Docker

Youtube video : https://www.youtube.com/watch?v=Ku1Da5uhbco

- Configure Freenas array in OpenSVC cluster
- Create volume template to provide protected storage to service
- Create Postgres in Docker template through cli
- Provision & test service
- Failover service
- Crash node & check LXC/Docker environments are failing back to other node

### opensvc.template.docker.pg.conf

OpenSVC service template to deploy Postgres through Docker container

### opensvc.template.vol.pool-over-freenas.conf

OpenSVC volume template describing a volume object serving 2 ZFS filesystems hosted in a mirrored ZFS pool, on top of 2 iscsi disks provisioned in Freenas array
