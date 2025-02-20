# Playbook

## Database - NCAE 

# Ports

PostgreSQL - 5432 

MySQL - 3306

## Networking 

a) tmui OR

Ip a to find interface

i) nmcli con mod enp0s3 ipv4.addresses 192.168.9.7/24

ii) nmcli con mod enp0s3 ipv4.gateway 192.168.9.1

iii) nmcli con mod enp0s3 ipv4.method manual

iv) nmcli con mod enp0s3 ipv4.dns “192.168.9.12”

v) nmcli con up enp0s3



firewalld might be up and running, does not allow 5432

i) check: sudo systemctl status firewalld

ii) firewall-cmd –zone=public –add-port=5432/tcp –-permanent

firewall-cmd --zone=public --add-port=5432/tcp --permanent


iii) firewall-cmd – reload

firewall-cmd --reload

To check 

firewall -cmd –list-all
