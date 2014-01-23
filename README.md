docker-pagespeed
================

Sample Dockerfile and Nginx configuration to run nginx + ngx_pagespeed. In the
current configuration, nginx acts as a reverse proxy. In future, this will also include
a working SPDY configuration.

Prior to building, please note that nginx config points to a non-existing site www.sample.com.
Change that with your own setup.

Build an image with
    docker build -t="nginx-pagespeed" -no-cache .

And start it with
    docker run -p 59080:80 -i -t nginx-pagespeed

For debugging & playing with nginx config on the image, do
    docker run -p 59080:80 -i -t nginx-defer /bin/bash
