
https://linux-audit.com/blocking-ip-addresses-in-linux-with-iptables/

https://superuser.com/questions/604998/monitor-tcp-traffic-on-specific-port/848966#848966


---
---


```
sudo iptables -I INPUT -s 141.98.7.14 -j DROP
```

ServerSeeker_net:
```
sudo iptables -I INPUT -s 109.123.240.84 -j DROP
```

mcsrvstat.us
```
sudo iptables -I INPUT -s 104.26.15.225 -j DROP
```
api.mcsrvstat.us
```
sudo iptables -I INPUT -s 172.67.71.106 -j DROP
```
Nei, ta det ved roten (spirit55555.dk)
```
sudo iptables -I INPUT -s 139.162.177.160 -j DROP
```
---
---

sudo docker buildx build -t begynnelse:1.0.15 .


sudo docker run --name begynnelse-1.0.15 --restart unless-stopped --volume ./data/public:/home/node/app/public --net proxiable --net-alias begynnelse -d begynnelse:1.0.15

---

sudo docker run --name fontrenamr-1.2.0 --restart unless-stopped --net proxiable --net-alias fontrenamr -d fontrenamr:latest

sudo docker run --name begynnelse-1.0.2-0 --restart unless-stopped --volume ./data/public:/home/node/app/public --net proxiable --net-alias begynnelse -d begynnelse:1.0.2-0

---

sudo docker buildx build -t admin-blokkdannelse -t admin-blokkdannelse:0.0.8 .

sudo docker run --name adm-blokkda-08 --restart unless-stopped --volume ./data/public:/home/node/app/public --volume ./data/logs:/home/node/app/logs --volume /opt/minecraft/.config:/home/node/.opt-minecraft -e MC_RCON_PW=\*\*\* --net proxiable --net-alias admin-blokkdannelse -d admin-blokkdannelse

sudo docker container rename admin-blokkdannelse-0.0.4 adm-blokkda

sudo docker exec -it admin-blokkdannelse-0.0.4 sh

---
---

```
[sudo] su -s /bin/bash -c ./checkpos minecraft
```


```

screen -p 0 -S mc-vault-hunters -X eval 'stuff "data get entity @p[name=Gaabananen] Pos"\015'

```

---

```
mcrcon -H blokkda.nnel.se -p ****** "list"
```
