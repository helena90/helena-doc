# docker compose startup
docker-compose -f docker-compose-nginx.yml up -d


# docker compose down
docker-compose -f docker-compose-nginx.yml down

# logs
docker logs -f --tail 10 home-nginx


# 인증서 발생
먼저 nginx down
certbot docker-compose 실행
nginx 다시 실행


# home certbot
DOMAIN=www.solena.kr docker-compose -f docker-compose-certbot.yml up
DOMAIN=blog.solena.kr docker-compose -f docker-compose-certbot.yml up


# clean
docker rm -f $(docker ps -a -q)