# Java ENV

Containers:

- MYSQL
- TOMCAT



###### Directory Structure

```
└─ java-env
   ├─ docker-compose.yml
   ├─ app
   ├─ mysql
   │  └─ my.cnf
   │  └─ data
   ├─ tomcat
      └─ server.xml
      └─ web.xml
```

`./app` : mapping to tomcat `webapps/ROOT` directory

`./mysql/my.cnf` : the config of MSYQL

 `./mysql/data/` : the data of MYSQL





### Arm supported

**mysql镜像**：biarms/mysql:5.7.30-linux-arm64v8

Reference : 

[树莓派4B使用docker安装mysql5.7.30](https://my.oschina.net/fastjrun/blog/4310625)

