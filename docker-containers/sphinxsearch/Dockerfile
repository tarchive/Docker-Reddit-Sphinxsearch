FROM debian:latest

RUN apt-get update
RUN apt-get install -y sphinxsearch
WORKDIR "/tmp"
RUN mkdir -p /etc/sphinxsearch
RUN mkdir -p /usr/sphinxsearch/data
ADD sphinx.conf /etc/sphinxsearch/sphinx.conf
EXPOSE 9312 9306
ENTRYPOINT ["/usr/bin/searchd","-c","/etc/sphinxsearch/sphinx.conf","--nodetach"]
