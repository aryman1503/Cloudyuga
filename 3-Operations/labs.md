## Docker

### Prerequisites for lab
- Create a Ubuntu VM instance on DigitalOcean. Please refer the `Setting up the lab` section of the course for details.
- Install Docker on the VM as given in `Chapter 4 - Container runtimes`.


### 1. How to search images on DockerHub ?

With `docker search` command we can list the available images on DockerHub. We can access the [DockerHub](hub.docker.com) from the browser and search.


```command
docker search nginx
```
```output
NAME                                     DESCRIPTION                                     STARS     OFFICIAL   AUTOMATED
nginx                                    Official build of Nginx.                        5289      [OK]
jwilder/nginx-proxy                      Automated Nginx reverse proxy for docker c...   943                  [OK]
richarvey/nginx-php-fpm                  Container running Nginx + PHP-FPM capable ...   343                  [OK]
jrcs/letsencrypt-nginx-proxy-companion   LetsEncrypt container to use with nginx as...   147                  [OK]
million12/nginx-php                      Nginx + PHP-FPM 5.5, 5.6, 7.0 (NG), CentOS...   75                   [OK]
webdevops/php-nginx                      Nginx with PHP-FPM                              69                   [OK]
.......
```

###  2. How to pull an image from DockerHub ?

To pull an image we can use `docker image pull` command.



```command
docker image pull nginx
```

