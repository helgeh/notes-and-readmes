# Serier jeg har

 - Skuddet på Toftøy
 - Kvinden med den tunge kuffert

# Proxyed serier
 - Kongen av Kongsberg
 - Roger Bullman
 - Avhørt: Torpedoen og milliardæren (1-16)
 - Avhørt: Skyldig til det motsatte er bevist (1-10)

# Last ned:



---

sudo docker buildx build -t begynnelse:1.0.17 .


sudo docker run --name begynnelse-1.0.17 --restart unless-stopped --volume ./data/public:/home/node/app/public --net proxiable --net-alias begynnelse -d begynnelse:1.0.17


