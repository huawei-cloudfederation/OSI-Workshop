<p align="center">
<h2> Basics of images and layers </h2>
</p>

#### Pulling basic nginx Image
```bash
docker pull saiakhil2012/nginx
```

#### See more details about basic nginx image
```bash
docker image inspect saiakhil2012/nginx
```

#### Pulling nginx with vim image
```bash
docker pull saiakhil2012/nginx:with_vim
```

#### See the more details about nginx with vim image
```bash
docker image inspect saiakhil2012/nginx:with_vim
```

<p align="center">
<h2> Let us see the advantage of Layers of Images Practically </h2>
</p>

#### Run a container as shown below
```bash
docker run -d --name enhanced_nginx saiakhil2012/enhanced_nginx
```

#### Get into the container
```bash
docker exec -it enhanced_nginx /bin/bash
```

#### Create a file
```bash
cd /home/
vim myfile.txt
Hello World
:wq
```

#### Exit out of Container
```bash
exit
```

#### Create an Image out of the running the container
```bash
docker commit -m "Added myfile.txt" <container_id> saiakhil2012/nginx:with_vim_myfile
```
#### List out the images
```bash
docker images
```

#### Remove other related containers and start a container with the new image
```bash
docker run -d --name nginx_with_vim_myfile saiakhil2012/nginx:with_vim_myfile
```

#### Get into the container
```bash
docker exec -it enhanced_nginx /bin/bash
```

#### Check our file
```bash
cd /home/
vim myfile.txt
:q
```

#### Exit out of Container
```bash
exit
```

#### See more into these images
```bash
docker image inspect saiakhil2012/nginx:with_vim_myfile
docker image inspect saiakhil2012/nginx:with_vim
```
#### Check the history of image
```bash
docker image history saiakhil2012/nginx:with_vim
docker image history saiakhil2012/nginx:with_vim_myfile

Observe the comment which we added before
```
