FROM postgres:17.6

USER root

RUN apt-get update && apt-get install -y \
    bsdutils \
    procps \
    iproute2 \
    netcat-openbsd \
    vim \
	binutils \
    less \
	curl \
    bsdmainutils \
	tmux \
	bc \
    && rm -rf /var/lib/apt/lists/*

RUN echo "alias ls='ls --color=auto'" >> /var/lib/postgresql/.bashrc

RUN echo "CREATE USER myuser WITH PASSWORD 'mypassword'; CREATE DATABASE mydatabase OWNER myuser;" > /docker-entrypoint-initdb.d/init.sql

EXPOSE 5432

USER postgres
