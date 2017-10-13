<p align="center">
<h2> Basics of Dockerfile </h2>
</p>

#### Create a Dockerfile

Use Hello World Dockerfile [here](hello_world_app/Dockerfile)
```bash
Save it to your current directory
```

#### Create a small Hello World html file
```bash
Use the Hello World html page here

(You can just have one line <h1>Hello World</h1>)
```

#### Build a Docker Image using the Dockerfile and html file
```bash
docker build -t nginx:with_website_v0 .
```

#### List the images
```bash
docker images

Our newly created image is present
```

#### Create a Docker Hub Account
<link>https://hub.docker.com/</link>

#### Login to Docker Account Just Created
```bash
docker login
Enter your credentials
```

#### Tag your image appropriately
```bash
docker tag <image_id> <username>/nginx:with_website_v0
```

#### Push your image to Your Public Docker Repository
```bash
docker push <username>/nginx:with_website_v0

Go to your repository :)
```

#### Remove your just created image and Pull it from Docker Hub
```bash
docker rmi <username>/nginx:with_website_v0
docker pull <username>/nginx:with_website_v0

If you already have an nginx image in you local, observe the layer optimization which we learnt in previous section
```

#### Run a container using created image
```bash
docker run -d -p 8091:80 --name my_container <username>/nginx:with_website_v0
```

#### Open your browser and check at port 8091
```bash
Hello World html is exposed
```

### Try It Out
Similar to the hello_wold_app, there are files for simple_app with all required elements [here](simple_app/)

```bash
Try creating your own image and push to your repo and run a container using it and expose a port 
Check what is shows !!! :)
```
