# NGINX with libModSecurity + ModSecurity-nginx connector

The dockerfile of this container has been copied from the [official nginx repo (alpine-perl variant)](https://github.com/nginxinc/docker-nginx/blob/1.15.9/mainline/alpine-perl/Dockerfile) and has been modified to add [ModSecurity library (v3)](https://github.com/SpiderLabs/ModSecurity/tree/v3/master) + [ModSecurity nginx connector](https://github.com/SpiderLabs/ModSecurity-nginx).

You can refer to the [official nginx image documentation](https://hub.docker.com/_/nginx/) for instructions on how to use this image.

When you provide your configuration you can enable modsecurity. Please refer to [their wiki](https://github.com/SpiderLabs/ModSecurity/wiki) for documentation.

NOTE: no rules are shipped with this container, if you enable modsecurity you need to provide your own


## Extras

If you're curious to know the difference from this dockerfile and the upstream one:

```bash
diff <(curl -fsL https://github.com/nginxinc/docker-nginx/raw/1.15.9/mainline/alpine-perl/Dockerfile) <(curl -fsL http://github.com/elisiano/docker-nginx-modsecurity/raw/master/Dockerfile)
```
