<p align="center">
<h2> Basics of Using Two Applications in Containerized Form </h2>
</p>

#### Let us create mysql container first
```bash
docker run --name wordpressdb -p 8095:3306 -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=wordpress -d saiakhil2012/mysql
```

#### Now Let us create the Wordpress Container
```bash
docker run -p 8099:80 -e WORDPRESS_DB_PASSWORD=password -d --name wordpress --link 
wordpressdb:mysql  saiakhil2012/wordpress
```

#### Now check the exposed port 8099 and Try Installing
```bash
This time it installs
```

#### Now let us see Posts Section
```bash
There is a Hello World Post
```

#### Let us get into the mysql container and edit the post content
```bash
docker exec -it wordpressdb /bin/bash
```

#### Check the mysql process
```bash
ps -ef| grep mysql
```

#### Use mysql
```bash
mysql -u root -p
use wordpress;
show tables;
describe wp_posts;
select post_content from wp_posts where post_content like "Welcome to Wordpress%";
update wp_posts set post_content="Welcome to Workshop powered by Huawei" where post_content like "Welcome to Wordpress%";
select post_content from wp_posts where post_content like "Welcome to%";
```

```bash
Check the updated Post Content at the exposed port
```

### Try It Out
```bash
Other way round also works (Change in Frontend and Backend it will get reflected)
```
