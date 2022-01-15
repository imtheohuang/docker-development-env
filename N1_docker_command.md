# N1 doccker contaniner command 

**arm64**



## Aria2 

``` shell
docker run -d \
  --name aria2-pro \
  --restart unless-stopped \
  --log-opt max-size=1m \
  -e PUID=$UID \
  -e PGID=$GID \
  -e UMASK_SET=022 \
  -e RPC_SECRET=123abcABC \
  -e RPC_PORT=6800 \
  -p 6800:6800 \
  -e LISTEN_PORT=6888 \
  -p 6888:6888 \
  -p 6888:6888/udp \
  -v /opt/docker-dir/aria2:/config \
  -v /mnt/H1/Share/Apps/Aria2:/downloads \
  p3terx/aria2-pro
```


## Ariang

```shell
docker run -d \
  --name ariang \
  --log-opt max-size=1m \
  --restart unless-stopped \
  -p 6880:6880 \
  p3terx/ariang

```



## Nginx

```shell
docker run -d --name nginx --restart always \
-p 80:80 \
-v /opt/docker-dir/nginx/html:/usr/share/nginx/html \
-v /opt/docker-dir/nginx/nginx.conf:/etc/nginx/nginx.conf \
-v /opt/docker-dir/nginx/conf:/etc/nginx/conf.d \
nginx
```



## TTnode

### zhang0510/ttnode-arm64

```bash
docker run -itd -v /mnt/H1/tangtian:/mnts --name ttnode --hostname ttnode --net=host --privileged=true --restart=always zhang0510/ttnode-arm64
```



### ericwang2006/ttnode

```  bash
docker run -itd --restart=always \
-v /mnt/H1/tangtian:/mnts \
-v /opt/docker-dir/ttnod/config:/config \
--name ttnode \
--hostname ttnode \
--net=host --privileged=true \
 ericwang2006/ttnode
```



## 未实践 `Image` *<u>wahyd4/aria2-ui</u>*: Aria2 + AriaNg + FileManager

```shell
docker run -d --name ariang \
  -p 80:80 \
  -p 443:443 \
  -e PUID=1000 \
  -e PGID=1000 \
  -e ENABLE_AUTH=true \
  -e RPC_SECRET=Hello \
  -e DOMAIN=https://example.com \
  -e ARIA2_SSL=false \
  -e ARIA2_USER=user \
  -e ARIA2_PWD=pwd \
  -e ARIA2_EXTERNAL_PORT=443 \
  -v /yourdata:/data \
  -v /app/a.db:/app/filebrowser.db \
  -v /yoursslkeys/:/app/conf/key \
  -v <the folder of aria2.conf and aria2.session>:/app/conf \
  wahyd4/aria2-ui
```



## 青龙

```shell
docker run -dit \
  -v /opt/docker-dir/qinglong/config:/ql/config \
  -v /opt/docker-dir/qinglong/log:/ql/log \
  -v /opt/docker-dir/qinglong/db:/ql/db \
  -v /opt/docker-dir/qinglong/repo:/ql/repo \
  -v /opt/docker-dir/qinglong/raw:/ql/raw \
  -v /opt/docker-dir/qinglong/scripts:/ql/scripts \
  -p 5700:5700 \
  --name qinglong \
  --hostname qinglong \
  --restart unless-stopped \
  whyour/qinglong:latest
```



### aliyundrive-webdav

```
docker run -d --name=aliyundrive-webdav --restart=unless-stopped -p 8080:8080 \
  -v /opt/aliyundrive-webdav/:/etc/aliyundrive-webdav/ \
  -e REFRESH_TOKEN='64b81df3887e4228a7dc851b3f463b71' \
  -e WEBDAV_AUTH_USER=admin \
  -e WEBDAV_AUTH_PASSWORD=123abcABC \
  messense/aliyundrive-webdav
```

