<p align="center">
<h2> Getting Started with Docker </h2>
</p>

#### Docker Client Help
```bash
docker help
```

#### Docker Client Specific Command Help
```bash
docker version --help
```

#### Version Information
```bash
docker version
```

#### System Level Info of Docker
```bash
docker info
```

#### Search an Image
```bash
docker search nginx
```

#### Running a container
```bash
docker run -d --name basic_nginx nginx
```

#### Get a list of docker conatiners
```bash
docker ps
```

#### Get a list of docker images
```bash
docker images
```

#### Getting into the Conatiner
```bash
docker exec -it basic_nginx /bin/bash
```

#### Basic Commands
```bash
date

whoami

ps -ef

vim
```


(Oops... it says "bash: vim: command not found")

#### Getting out of the container
```bash
exit
```

#### Run an enhanced nginx
```bash
docker run -d --name enhanced_nginx saiakhil2012/nginx:with_vim
```

#### Getting into the Conatiner
```bash
docker exec -it enhanced_nginx /bin/bash
```

#### Basic Commands
```bash
date

whoami

ps -ef

vim
```

(This time vim works :) )
