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



