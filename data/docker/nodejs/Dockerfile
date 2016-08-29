FROM phusion/passenger-nodejs:0.9.19
MAINTAINER Andreas Ruck

# Set correct environment variables.
ENV HOME /root

# Use baseimage-docker's init process.
CMD ["/sbin/my_init"]

# remove default nginx site and activate built-in nginx
RUN rm /etc/nginx/sites-enabled/default
RUN rm -f /etc/service/nginx/down

# Make project dir and make webapp.conf available to nginx
RUN mkdir /home/app/webapp
ADD webapp.conf /etc/nginx/sites-enabled/webapp.conf


# cleanup after ourselves
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
