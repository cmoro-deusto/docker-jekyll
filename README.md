docker-jekyll
=============

## Customize your locales

    RUN locale-gen en_GB.UTF-8
    ENV LANG en_GB.UTF-8
    ENV LC_CTYPE en_GB.UTF-8


Run the container
=================

Run the docker container (will be removed when exit), map localhost 4000 port to
container 4000 port, and our /home/dordoka/Code/ path to /home/octopress/Code
container path:

    docker run --rm -it -p 4000:4000 -v /home/dordoka/Code/:/home/jekyll/Code dordoka/jekyll
