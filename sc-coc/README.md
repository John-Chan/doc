# Build

## get srouce code
```
git clone --recursive <url>
```

## update with submodules
```
git submodule update --recursive --remote
```

To build docker images,you need install docker first.
> see [Install Docker](https://docs.docker.com/install/) 

### For Windows

run `build-docker-all.cmd` to build docker images,or run `build-jar-all.cmd` for jar packages.

### For Linux
```
chmod +x *.sh
```

run `build-docker-all.sh` to build docker images,or run `build-jar-all.sh` for jar packages.


# Deploy


Firest,You need setup :
- database for service (checkout application.yml for each serivce) 
- git repository to host configuration files,config file templates: `\system\config\src\main\resources\config`


### docker( minimize )
`minimize` means single instance for all service

see shell script in `it-ops/mini/linux-docker`.

# Test

- rabbit mq management: http:\\your-ip-address:15672.(default user/password :guest/guest)
- eureka : http://your-ip-address:8761/
- admin(Spring Boot) : http://your-ip-address:18002/
- swagger ui: http://your-ip-address:service-port/swagger-ui.html

# screen

![docker-images](../screen/2018-04-28/docker-images.PNG)

![eureka](../screen/2018-04-28/eureka.PNG)

![admin](../screen/2018-04-28/admin.PNG)

![rabbit](../screen/2018-04-28/rabbit.PNG)

# NOTE: 

- no front end (web server) currently
- So,What does this program do?download game data,lots of data,then find something fun.

