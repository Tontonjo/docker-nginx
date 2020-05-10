# Tonton Jo - 2020
# Join me on Youtube: https://www.youtube.com/channel/UCnED3K6K5FDUp-x_8rwpsZw

Quick startup guide:

1: Copy, clone thoses files where you want them to be.
git clone https://github.com/Tontonjo/docker-nginx.git

2: Edit the files to match your domain / target environnement uncomment ssl settings if needed

3: start the container
docker run -d --name nginx --restart unless-stopped -v /target/path/nginx:/etc/nginx/ -p 80:80 -p 443:443 nginx

4: check logs: no output means everything looks fine 
docker logs -f nginx

5:To reload conf without having to reboot container:
docker exec -it nginx /etc/init.d/nginx reload



