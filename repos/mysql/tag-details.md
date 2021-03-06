<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:8.0.0`](#mysql800)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8`](#mysql8)
-	[`mysql:5.7.17`](#mysql5717)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5`](#mysql5)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:5.6.35`](#mysql5635)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.5.54`](#mysql5554)
-	[`mysql:5.5`](#mysql55)

## `mysql:8.0.0`

```console
$ docker pull mysql@sha256:ad4e2635b7f0561737407e5b4b9a26f2931ab506f3a91b840e6caa94c7e70b81
```

-	Platforms:
	-	linux; amd64

### `mysql:8.0.0` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 MB (129663655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1e9e70a4a414060ed85f9ffbc818a8629a32749c0454142be44bf70688d5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:00:10 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Dec 2016 01:00:11 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 01:00:29 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 14 Dec 2016 01:00:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Dec 2016 02:47:50 GMT
RUN apt-get update && apt-get install -y perl pwgen --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 02:47:52 GMT
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys A4A9406876FCBD3C456770C88C718D3B5072E1F5
# Wed, 14 Dec 2016 02:50:40 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Dec 2016 02:50:40 GMT
ENV MYSQL_VERSION=8.0.0-dmr-1debian8
# Wed, 14 Dec 2016 02:50:42 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 14 Dec 2016 02:51:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 14 Dec 2016 02:51:16 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/mysql.conf.d/mysqld.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 14 Dec 2016 02:51:16 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Dec 2016 02:51:17 GMT
COPY file:fc6fa63e59403864ccd3dc0d09d92a9b3feb07f725587a6f97309cf96bb52a6b in /usr/local/bin/ 
# Wed, 14 Dec 2016 02:51:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Dec 2016 02:51:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Dec 2016 02:51:19 GMT
EXPOSE 3306/tcp
# Wed, 14 Dec 2016 02:51:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d5846e536af54d4f4773fb5173c759fb8b3673a34710a7e1fe15b4120dc8d2`  
		Last Modified: Wed, 14 Dec 2016 03:24:37 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e9152a1702d9b527b4e753786743d20ceea693424429f5da60410d7b02ddf`  
		Last Modified: Wed, 14 Dec 2016 03:24:36 GMT  
		Size: 1.2 MB (1216944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832e6b0304969b9baa6a38a8e32da0aaf7d7cbf9476c31d006f335264edc6147`  
		Last Modified: Wed, 14 Dec 2016 01:03:50 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4a6c835905c74aa7540cb63201fb2b87287ea2e7fdba0513db04dddfed1e95`  
		Last Modified: Wed, 14 Dec 2016 03:28:16 GMT  
		Size: 8.2 MB (8248277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f247e29ab116e18d92039c22d47021d968a34eb21c25aa3d3beb9d57182038`  
		Last Modified: Wed, 14 Dec 2016 03:28:11 GMT  
		Size: 19.0 KB (19020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f17db635ae79c261a9c96c95f08113b4945dc0e908734a49ff47c83346fd5db`  
		Last Modified: Wed, 14 Dec 2016 03:28:09 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0663c149b918114b8c71cf8e18c01e7f43be2a443c3f4c73f7a0dd48213038`  
		Last Modified: Wed, 14 Dec 2016 03:28:32 GMT  
		Size: 68.8 MB (68810783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323a2b791e20e91cdb7cadf742af9d3c51ca39b6be4a6d8bdafc880dc840b8e1`  
		Last Modified: Wed, 14 Dec 2016 03:28:08 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84c6d36b64109b81900141ddbc242094f0ed2f21e81df702cfabf8093b08e57`  
		Last Modified: Wed, 14 Dec 2016 03:28:07 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e97c86715a7de176382e5e0f73afa5134cc0d2d2cf9318941e153c59c4353c`  
		Last Modified: Wed, 14 Dec 2016 03:28:09 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:ad4e2635b7f0561737407e5b4b9a26f2931ab506f3a91b840e6caa94c7e70b81
```

-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 MB (129663655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1e9e70a4a414060ed85f9ffbc818a8629a32749c0454142be44bf70688d5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:00:10 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Dec 2016 01:00:11 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 01:00:29 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 14 Dec 2016 01:00:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Dec 2016 02:47:50 GMT
RUN apt-get update && apt-get install -y perl pwgen --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 02:47:52 GMT
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys A4A9406876FCBD3C456770C88C718D3B5072E1F5
# Wed, 14 Dec 2016 02:50:40 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Dec 2016 02:50:40 GMT
ENV MYSQL_VERSION=8.0.0-dmr-1debian8
# Wed, 14 Dec 2016 02:50:42 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 14 Dec 2016 02:51:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 14 Dec 2016 02:51:16 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/mysql.conf.d/mysqld.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 14 Dec 2016 02:51:16 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Dec 2016 02:51:17 GMT
COPY file:fc6fa63e59403864ccd3dc0d09d92a9b3feb07f725587a6f97309cf96bb52a6b in /usr/local/bin/ 
# Wed, 14 Dec 2016 02:51:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Dec 2016 02:51:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Dec 2016 02:51:19 GMT
EXPOSE 3306/tcp
# Wed, 14 Dec 2016 02:51:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d5846e536af54d4f4773fb5173c759fb8b3673a34710a7e1fe15b4120dc8d2`  
		Last Modified: Wed, 14 Dec 2016 03:24:37 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e9152a1702d9b527b4e753786743d20ceea693424429f5da60410d7b02ddf`  
		Last Modified: Wed, 14 Dec 2016 03:24:36 GMT  
		Size: 1.2 MB (1216944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832e6b0304969b9baa6a38a8e32da0aaf7d7cbf9476c31d006f335264edc6147`  
		Last Modified: Wed, 14 Dec 2016 01:03:50 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4a6c835905c74aa7540cb63201fb2b87287ea2e7fdba0513db04dddfed1e95`  
		Last Modified: Wed, 14 Dec 2016 03:28:16 GMT  
		Size: 8.2 MB (8248277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f247e29ab116e18d92039c22d47021d968a34eb21c25aa3d3beb9d57182038`  
		Last Modified: Wed, 14 Dec 2016 03:28:11 GMT  
		Size: 19.0 KB (19020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f17db635ae79c261a9c96c95f08113b4945dc0e908734a49ff47c83346fd5db`  
		Last Modified: Wed, 14 Dec 2016 03:28:09 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0663c149b918114b8c71cf8e18c01e7f43be2a443c3f4c73f7a0dd48213038`  
		Last Modified: Wed, 14 Dec 2016 03:28:32 GMT  
		Size: 68.8 MB (68810783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323a2b791e20e91cdb7cadf742af9d3c51ca39b6be4a6d8bdafc880dc840b8e1`  
		Last Modified: Wed, 14 Dec 2016 03:28:08 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84c6d36b64109b81900141ddbc242094f0ed2f21e81df702cfabf8093b08e57`  
		Last Modified: Wed, 14 Dec 2016 03:28:07 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e97c86715a7de176382e5e0f73afa5134cc0d2d2cf9318941e153c59c4353c`  
		Last Modified: Wed, 14 Dec 2016 03:28:09 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:ad4e2635b7f0561737407e5b4b9a26f2931ab506f3a91b840e6caa94c7e70b81
```

-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 MB (129663655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1e9e70a4a414060ed85f9ffbc818a8629a32749c0454142be44bf70688d5e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:00:10 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Dec 2016 01:00:11 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 01:00:29 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 14 Dec 2016 01:00:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Dec 2016 02:47:50 GMT
RUN apt-get update && apt-get install -y perl pwgen --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 02:47:52 GMT
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys A4A9406876FCBD3C456770C88C718D3B5072E1F5
# Wed, 14 Dec 2016 02:50:40 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 14 Dec 2016 02:50:40 GMT
ENV MYSQL_VERSION=8.0.0-dmr-1debian8
# Wed, 14 Dec 2016 02:50:42 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 14 Dec 2016 02:51:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 14 Dec 2016 02:51:16 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/mysql.conf.d/mysqld.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 14 Dec 2016 02:51:16 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Dec 2016 02:51:17 GMT
COPY file:fc6fa63e59403864ccd3dc0d09d92a9b3feb07f725587a6f97309cf96bb52a6b in /usr/local/bin/ 
# Wed, 14 Dec 2016 02:51:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Dec 2016 02:51:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Dec 2016 02:51:19 GMT
EXPOSE 3306/tcp
# Wed, 14 Dec 2016 02:51:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d5846e536af54d4f4773fb5173c759fb8b3673a34710a7e1fe15b4120dc8d2`  
		Last Modified: Wed, 14 Dec 2016 03:24:37 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e9152a1702d9b527b4e753786743d20ceea693424429f5da60410d7b02ddf`  
		Last Modified: Wed, 14 Dec 2016 03:24:36 GMT  
		Size: 1.2 MB (1216944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832e6b0304969b9baa6a38a8e32da0aaf7d7cbf9476c31d006f335264edc6147`  
		Last Modified: Wed, 14 Dec 2016 01:03:50 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4a6c835905c74aa7540cb63201fb2b87287ea2e7fdba0513db04dddfed1e95`  
		Last Modified: Wed, 14 Dec 2016 03:28:16 GMT  
		Size: 8.2 MB (8248277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f247e29ab116e18d92039c22d47021d968a34eb21c25aa3d3beb9d57182038`  
		Last Modified: Wed, 14 Dec 2016 03:28:11 GMT  
		Size: 19.0 KB (19020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f17db635ae79c261a9c96c95f08113b4945dc0e908734a49ff47c83346fd5db`  
		Last Modified: Wed, 14 Dec 2016 03:28:09 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0663c149b918114b8c71cf8e18c01e7f43be2a443c3f4c73f7a0dd48213038`  
		Last Modified: Wed, 14 Dec 2016 03:28:32 GMT  
		Size: 68.8 MB (68810783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323a2b791e20e91cdb7cadf742af9d3c51ca39b6be4a6d8bdafc880dc840b8e1`  
		Last Modified: Wed, 14 Dec 2016 03:28:08 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84c6d36b64109b81900141ddbc242094f0ed2f21e81df702cfabf8093b08e57`  
		Last Modified: Wed, 14 Dec 2016 03:28:07 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e97c86715a7de176382e5e0f73afa5134cc0d2d2cf9318941e153c59c4353c`  
		Last Modified: Wed, 14 Dec 2016 03:28:09 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.17`

```console
$ docker pull mysql@sha256:de1570492c641112fdb94db9c788f6a400f71f25a920da95ec88c3848450ed57
```

-	Platforms:
	-	linux; amd64

### `mysql:5.7.17` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137831953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594dc21de8de7cdae01ecbd4d8a4dedead73756984896a00fce13cbc8c24f38e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:00:10 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Dec 2016 01:00:11 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 01:00:29 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 14 Dec 2016 01:00:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Dec 2016 02:47:50 GMT
RUN apt-get update && apt-get install -y perl pwgen --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 02:47:52 GMT
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys A4A9406876FCBD3C456770C88C718D3B5072E1F5
# Wed, 14 Dec 2016 02:47:53 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 14 Dec 2016 02:47:53 GMT
ENV MYSQL_VERSION=5.7.17-1debian8
# Wed, 14 Dec 2016 02:47:54 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 14 Dec 2016 02:48:17 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 14 Dec 2016 02:48:23 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/mysql.conf.d/mysqld.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 14 Dec 2016 02:48:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Dec 2016 02:48:24 GMT
COPY file:fc6fa63e59403864ccd3dc0d09d92a9b3feb07f725587a6f97309cf96bb52a6b in /usr/local/bin/ 
# Wed, 14 Dec 2016 02:48:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Dec 2016 02:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Dec 2016 02:48:26 GMT
EXPOSE 3306/tcp
# Wed, 14 Dec 2016 02:48:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d5846e536af54d4f4773fb5173c759fb8b3673a34710a7e1fe15b4120dc8d2`  
		Last Modified: Wed, 14 Dec 2016 03:24:37 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e9152a1702d9b527b4e753786743d20ceea693424429f5da60410d7b02ddf`  
		Last Modified: Wed, 14 Dec 2016 03:24:36 GMT  
		Size: 1.2 MB (1216944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832e6b0304969b9baa6a38a8e32da0aaf7d7cbf9476c31d006f335264edc6147`  
		Last Modified: Wed, 14 Dec 2016 01:03:50 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4a6c835905c74aa7540cb63201fb2b87287ea2e7fdba0513db04dddfed1e95`  
		Last Modified: Wed, 14 Dec 2016 03:28:16 GMT  
		Size: 8.2 MB (8248277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f247e29ab116e18d92039c22d47021d968a34eb21c25aa3d3beb9d57182038`  
		Last Modified: Wed, 14 Dec 2016 03:28:11 GMT  
		Size: 19.0 KB (19020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21be3e56207166d0b71bdb3ad23e6db98386fe5311bfb2766059d8a0856f4f61`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7399d6bf03330f82cb32f3dca0c4b298b5d89a1c90c2f2a2d56182222bc58de`  
		Last Modified: Wed, 14 Dec 2016 03:29:52 GMT  
		Size: 77.0 MB (76979027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdaeae6c735d31cbab37e1f9aa3a25ca1c6123d7332d5262c391f7c14f305d7`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 936.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3835a628a92fe32c0dfa6c19fefc601d174de802257e8c15ba3124ba799d5a1a`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530d0fb19b1345d71e220bd57e752a77a9eaec3d49c7ec806ec858f020ddc1ec`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:de1570492c641112fdb94db9c788f6a400f71f25a920da95ec88c3848450ed57
```

-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137831953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594dc21de8de7cdae01ecbd4d8a4dedead73756984896a00fce13cbc8c24f38e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:00:10 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Dec 2016 01:00:11 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 01:00:29 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 14 Dec 2016 01:00:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Dec 2016 02:47:50 GMT
RUN apt-get update && apt-get install -y perl pwgen --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 02:47:52 GMT
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys A4A9406876FCBD3C456770C88C718D3B5072E1F5
# Wed, 14 Dec 2016 02:47:53 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 14 Dec 2016 02:47:53 GMT
ENV MYSQL_VERSION=5.7.17-1debian8
# Wed, 14 Dec 2016 02:47:54 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 14 Dec 2016 02:48:17 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 14 Dec 2016 02:48:23 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/mysql.conf.d/mysqld.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 14 Dec 2016 02:48:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Dec 2016 02:48:24 GMT
COPY file:fc6fa63e59403864ccd3dc0d09d92a9b3feb07f725587a6f97309cf96bb52a6b in /usr/local/bin/ 
# Wed, 14 Dec 2016 02:48:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Dec 2016 02:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Dec 2016 02:48:26 GMT
EXPOSE 3306/tcp
# Wed, 14 Dec 2016 02:48:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d5846e536af54d4f4773fb5173c759fb8b3673a34710a7e1fe15b4120dc8d2`  
		Last Modified: Wed, 14 Dec 2016 03:24:37 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e9152a1702d9b527b4e753786743d20ceea693424429f5da60410d7b02ddf`  
		Last Modified: Wed, 14 Dec 2016 03:24:36 GMT  
		Size: 1.2 MB (1216944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832e6b0304969b9baa6a38a8e32da0aaf7d7cbf9476c31d006f335264edc6147`  
		Last Modified: Wed, 14 Dec 2016 01:03:50 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4a6c835905c74aa7540cb63201fb2b87287ea2e7fdba0513db04dddfed1e95`  
		Last Modified: Wed, 14 Dec 2016 03:28:16 GMT  
		Size: 8.2 MB (8248277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f247e29ab116e18d92039c22d47021d968a34eb21c25aa3d3beb9d57182038`  
		Last Modified: Wed, 14 Dec 2016 03:28:11 GMT  
		Size: 19.0 KB (19020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21be3e56207166d0b71bdb3ad23e6db98386fe5311bfb2766059d8a0856f4f61`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7399d6bf03330f82cb32f3dca0c4b298b5d89a1c90c2f2a2d56182222bc58de`  
		Last Modified: Wed, 14 Dec 2016 03:29:52 GMT  
		Size: 77.0 MB (76979027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdaeae6c735d31cbab37e1f9aa3a25ca1c6123d7332d5262c391f7c14f305d7`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 936.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3835a628a92fe32c0dfa6c19fefc601d174de802257e8c15ba3124ba799d5a1a`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530d0fb19b1345d71e220bd57e752a77a9eaec3d49c7ec806ec858f020ddc1ec`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5`

```console
$ docker pull mysql@sha256:de1570492c641112fdb94db9c788f6a400f71f25a920da95ec88c3848450ed57
```

-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137831953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594dc21de8de7cdae01ecbd4d8a4dedead73756984896a00fce13cbc8c24f38e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:00:10 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Dec 2016 01:00:11 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 01:00:29 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 14 Dec 2016 01:00:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Dec 2016 02:47:50 GMT
RUN apt-get update && apt-get install -y perl pwgen --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 02:47:52 GMT
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys A4A9406876FCBD3C456770C88C718D3B5072E1F5
# Wed, 14 Dec 2016 02:47:53 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 14 Dec 2016 02:47:53 GMT
ENV MYSQL_VERSION=5.7.17-1debian8
# Wed, 14 Dec 2016 02:47:54 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 14 Dec 2016 02:48:17 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 14 Dec 2016 02:48:23 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/mysql.conf.d/mysqld.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 14 Dec 2016 02:48:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Dec 2016 02:48:24 GMT
COPY file:fc6fa63e59403864ccd3dc0d09d92a9b3feb07f725587a6f97309cf96bb52a6b in /usr/local/bin/ 
# Wed, 14 Dec 2016 02:48:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Dec 2016 02:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Dec 2016 02:48:26 GMT
EXPOSE 3306/tcp
# Wed, 14 Dec 2016 02:48:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d5846e536af54d4f4773fb5173c759fb8b3673a34710a7e1fe15b4120dc8d2`  
		Last Modified: Wed, 14 Dec 2016 03:24:37 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e9152a1702d9b527b4e753786743d20ceea693424429f5da60410d7b02ddf`  
		Last Modified: Wed, 14 Dec 2016 03:24:36 GMT  
		Size: 1.2 MB (1216944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832e6b0304969b9baa6a38a8e32da0aaf7d7cbf9476c31d006f335264edc6147`  
		Last Modified: Wed, 14 Dec 2016 01:03:50 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4a6c835905c74aa7540cb63201fb2b87287ea2e7fdba0513db04dddfed1e95`  
		Last Modified: Wed, 14 Dec 2016 03:28:16 GMT  
		Size: 8.2 MB (8248277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f247e29ab116e18d92039c22d47021d968a34eb21c25aa3d3beb9d57182038`  
		Last Modified: Wed, 14 Dec 2016 03:28:11 GMT  
		Size: 19.0 KB (19020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21be3e56207166d0b71bdb3ad23e6db98386fe5311bfb2766059d8a0856f4f61`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7399d6bf03330f82cb32f3dca0c4b298b5d89a1c90c2f2a2d56182222bc58de`  
		Last Modified: Wed, 14 Dec 2016 03:29:52 GMT  
		Size: 77.0 MB (76979027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdaeae6c735d31cbab37e1f9aa3a25ca1c6123d7332d5262c391f7c14f305d7`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 936.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3835a628a92fe32c0dfa6c19fefc601d174de802257e8c15ba3124ba799d5a1a`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530d0fb19b1345d71e220bd57e752a77a9eaec3d49c7ec806ec858f020ddc1ec`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:de1570492c641112fdb94db9c788f6a400f71f25a920da95ec88c3848450ed57
```

-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137831953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594dc21de8de7cdae01ecbd4d8a4dedead73756984896a00fce13cbc8c24f38e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:00:10 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Dec 2016 01:00:11 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 01:00:29 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 14 Dec 2016 01:00:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Dec 2016 02:47:50 GMT
RUN apt-get update && apt-get install -y perl pwgen --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 02:47:52 GMT
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys A4A9406876FCBD3C456770C88C718D3B5072E1F5
# Wed, 14 Dec 2016 02:47:53 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 14 Dec 2016 02:47:53 GMT
ENV MYSQL_VERSION=5.7.17-1debian8
# Wed, 14 Dec 2016 02:47:54 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 14 Dec 2016 02:48:17 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 14 Dec 2016 02:48:23 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/mysql.conf.d/mysqld.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 14 Dec 2016 02:48:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Dec 2016 02:48:24 GMT
COPY file:fc6fa63e59403864ccd3dc0d09d92a9b3feb07f725587a6f97309cf96bb52a6b in /usr/local/bin/ 
# Wed, 14 Dec 2016 02:48:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Dec 2016 02:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Dec 2016 02:48:26 GMT
EXPOSE 3306/tcp
# Wed, 14 Dec 2016 02:48:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d5846e536af54d4f4773fb5173c759fb8b3673a34710a7e1fe15b4120dc8d2`  
		Last Modified: Wed, 14 Dec 2016 03:24:37 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e9152a1702d9b527b4e753786743d20ceea693424429f5da60410d7b02ddf`  
		Last Modified: Wed, 14 Dec 2016 03:24:36 GMT  
		Size: 1.2 MB (1216944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832e6b0304969b9baa6a38a8e32da0aaf7d7cbf9476c31d006f335264edc6147`  
		Last Modified: Wed, 14 Dec 2016 01:03:50 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4a6c835905c74aa7540cb63201fb2b87287ea2e7fdba0513db04dddfed1e95`  
		Last Modified: Wed, 14 Dec 2016 03:28:16 GMT  
		Size: 8.2 MB (8248277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f247e29ab116e18d92039c22d47021d968a34eb21c25aa3d3beb9d57182038`  
		Last Modified: Wed, 14 Dec 2016 03:28:11 GMT  
		Size: 19.0 KB (19020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21be3e56207166d0b71bdb3ad23e6db98386fe5311bfb2766059d8a0856f4f61`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7399d6bf03330f82cb32f3dca0c4b298b5d89a1c90c2f2a2d56182222bc58de`  
		Last Modified: Wed, 14 Dec 2016 03:29:52 GMT  
		Size: 77.0 MB (76979027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdaeae6c735d31cbab37e1f9aa3a25ca1c6123d7332d5262c391f7c14f305d7`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 936.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3835a628a92fe32c0dfa6c19fefc601d174de802257e8c15ba3124ba799d5a1a`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 2.1 KB (2132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530d0fb19b1345d71e220bd57e752a77a9eaec3d49c7ec806ec858f020ddc1ec`  
		Last Modified: Wed, 14 Dec 2016 03:29:25 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.35`

```console
$ docker pull mysql@sha256:afbd1708374fb8e5fa68c11c23be53a43a797ede4c04d399dd04b8893b2e75e2
```

-	Platforms:
	-	linux; amd64

### `mysql:5.6.35` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112788681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1406e1f7c42c7e664e138c2cedfcd4c09eef6d4859df1f93fd54d87ed3ba1a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:00:10 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Dec 2016 01:00:11 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 01:00:29 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 14 Dec 2016 01:00:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Dec 2016 02:47:50 GMT
RUN apt-get update && apt-get install -y perl pwgen --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 02:47:52 GMT
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys A4A9406876FCBD3C456770C88C718D3B5072E1F5
# Wed, 14 Dec 2016 02:50:06 GMT
ENV MYSQL_MAJOR=5.6
# Wed, 14 Dec 2016 02:50:06 GMT
ENV MYSQL_VERSION=5.6.35-1debian8
# Wed, 14 Dec 2016 02:50:07 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 14 Dec 2016 02:50:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 14 Dec 2016 02:50:36 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/my.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 14 Dec 2016 02:50:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Dec 2016 02:50:37 GMT
COPY file:603f69aa45f7824bbbaa8d837fcd5ea1da2df9450f342a1046ba7e0d6cecaa4f in /usr/local/bin/ 
# Wed, 14 Dec 2016 02:50:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Dec 2016 02:50:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Dec 2016 02:50:39 GMT
EXPOSE 3306/tcp
# Wed, 14 Dec 2016 02:50:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d5846e536af54d4f4773fb5173c759fb8b3673a34710a7e1fe15b4120dc8d2`  
		Last Modified: Wed, 14 Dec 2016 03:24:37 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e9152a1702d9b527b4e753786743d20ceea693424429f5da60410d7b02ddf`  
		Last Modified: Wed, 14 Dec 2016 03:24:36 GMT  
		Size: 1.2 MB (1216944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832e6b0304969b9baa6a38a8e32da0aaf7d7cbf9476c31d006f335264edc6147`  
		Last Modified: Wed, 14 Dec 2016 01:03:50 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4a6c835905c74aa7540cb63201fb2b87287ea2e7fdba0513db04dddfed1e95`  
		Last Modified: Wed, 14 Dec 2016 03:28:16 GMT  
		Size: 8.2 MB (8248277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f247e29ab116e18d92039c22d47021d968a34eb21c25aa3d3beb9d57182038`  
		Last Modified: Wed, 14 Dec 2016 03:28:11 GMT  
		Size: 19.0 KB (19020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f88d2008c200871e2a2ad64e7fd611d263b79f94fed7c5d8b9335f9d62f424`  
		Last Modified: Wed, 14 Dec 2016 03:30:59 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb591b4395b518ac9d1c6d2ac3b86e976709df30022bb7734c992a263271cf55`  
		Last Modified: Wed, 14 Dec 2016 03:31:18 GMT  
		Size: 51.9 MB (51935436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da36fdc89c53606f2081c1028188d1d515c408ec59ed9fa15ad28830d7e942b5`  
		Last Modified: Wed, 14 Dec 2016 03:30:59 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2a78a37dc6e03875f6b03898d33de7b4e7f6f72a61e06474ba025092123089`  
		Last Modified: Wed, 14 Dec 2016 03:30:59 GMT  
		Size: 2.2 KB (2173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9126ae2ee3609bed5fde9ceb548edaffef2bd315a5a00fb51b045997647dae4`  
		Last Modified: Wed, 14 Dec 2016 03:30:59 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:afbd1708374fb8e5fa68c11c23be53a43a797ede4c04d399dd04b8893b2e75e2
```

-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112788681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1406e1f7c42c7e664e138c2cedfcd4c09eef6d4859df1f93fd54d87ed3ba1a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:00:10 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Dec 2016 01:00:11 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 01:00:29 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 14 Dec 2016 01:00:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Dec 2016 02:47:50 GMT
RUN apt-get update && apt-get install -y perl pwgen --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 02:47:52 GMT
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys A4A9406876FCBD3C456770C88C718D3B5072E1F5
# Wed, 14 Dec 2016 02:50:06 GMT
ENV MYSQL_MAJOR=5.6
# Wed, 14 Dec 2016 02:50:06 GMT
ENV MYSQL_VERSION=5.6.35-1debian8
# Wed, 14 Dec 2016 02:50:07 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Wed, 14 Dec 2016 02:50:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 14 Dec 2016 02:50:36 GMT
RUN sed -Ei 's/^(bind-address|log)/#&/' /etc/mysql/my.cnf 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Wed, 14 Dec 2016 02:50:36 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Dec 2016 02:50:37 GMT
COPY file:603f69aa45f7824bbbaa8d837fcd5ea1da2df9450f342a1046ba7e0d6cecaa4f in /usr/local/bin/ 
# Wed, 14 Dec 2016 02:50:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Dec 2016 02:50:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Dec 2016 02:50:39 GMT
EXPOSE 3306/tcp
# Wed, 14 Dec 2016 02:50:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d5846e536af54d4f4773fb5173c759fb8b3673a34710a7e1fe15b4120dc8d2`  
		Last Modified: Wed, 14 Dec 2016 03:24:37 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e9152a1702d9b527b4e753786743d20ceea693424429f5da60410d7b02ddf`  
		Last Modified: Wed, 14 Dec 2016 03:24:36 GMT  
		Size: 1.2 MB (1216944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832e6b0304969b9baa6a38a8e32da0aaf7d7cbf9476c31d006f335264edc6147`  
		Last Modified: Wed, 14 Dec 2016 01:03:50 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4a6c835905c74aa7540cb63201fb2b87287ea2e7fdba0513db04dddfed1e95`  
		Last Modified: Wed, 14 Dec 2016 03:28:16 GMT  
		Size: 8.2 MB (8248277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f247e29ab116e18d92039c22d47021d968a34eb21c25aa3d3beb9d57182038`  
		Last Modified: Wed, 14 Dec 2016 03:28:11 GMT  
		Size: 19.0 KB (19020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f88d2008c200871e2a2ad64e7fd611d263b79f94fed7c5d8b9335f9d62f424`  
		Last Modified: Wed, 14 Dec 2016 03:30:59 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb591b4395b518ac9d1c6d2ac3b86e976709df30022bb7734c992a263271cf55`  
		Last Modified: Wed, 14 Dec 2016 03:31:18 GMT  
		Size: 51.9 MB (51935436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da36fdc89c53606f2081c1028188d1d515c408ec59ed9fa15ad28830d7e942b5`  
		Last Modified: Wed, 14 Dec 2016 03:30:59 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2a78a37dc6e03875f6b03898d33de7b4e7f6f72a61e06474ba025092123089`  
		Last Modified: Wed, 14 Dec 2016 03:30:59 GMT  
		Size: 2.2 KB (2173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9126ae2ee3609bed5fde9ceb548edaffef2bd315a5a00fb51b045997647dae4`  
		Last Modified: Wed, 14 Dec 2016 03:30:59 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.5.54`

```console
$ docker pull mysql@sha256:7af3fe3e7e2dc23df2768eb340fc656af145f48efd0137113a435606566344d3
```

-	Platforms:
	-	linux; amd64

### `mysql:5.5.54` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87414704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8cd588fa9c6441f682393dd9f200046c28d176d524c11979ec64d81261fd59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:00:10 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Dec 2016 01:00:11 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 01:00:29 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 14 Dec 2016 01:00:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Dec 2016 02:48:34 GMT
RUN apt-get update && apt-get install -y perl --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 02:48:41 GMT
RUN apt-get update && apt-get install -y libaio1 pwgen && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 02:48:50 GMT
ENV MYSQL_MAJOR=5.5
# Wed, 14 Dec 2016 02:48:50 GMT
ENV MYSQL_VERSION=5.5.54
# Wed, 14 Dec 2016 02:49:40 GMT
RUN apt-get update && apt-get install -y ca-certificates wget --no-install-recommends && rm -rf /var/lib/apt/lists/* 	&& wget "https://cdn.mysql.com/Downloads/MySQL-$MYSQL_MAJOR/mysql-$MYSQL_VERSION-linux2.6-x86_64.tar.gz" -O mysql.tar.gz 	&& wget "https://cdn.mysql.com/Downloads/MySQL-$MYSQL_MAJOR/mysql-$MYSQL_VERSION-linux2.6-x86_64.tar.gz.asc" -O mysql.tar.gz.asc 	&& apt-get purge -y --auto-remove ca-certificates wget 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys A4A9406876FCBD3C456770C88C718D3B5072E1F5 	&& gpg --batch --verify mysql.tar.gz.asc mysql.tar.gz 	&& rm -r "$GNUPGHOME" mysql.tar.gz.asc 	&& mkdir /usr/local/mysql 	&& tar -xzf mysql.tar.gz -C /usr/local/mysql --strip-components=1 	&& rm mysql.tar.gz 	&& rm -rf /usr/local/mysql/mysql-test /usr/local/mysql/sql-bench 	&& rm -rf /usr/local/mysql/bin/*-debug /usr/local/mysql/bin/*_embedded 	&& find /usr/local/mysql -type f -name "*.a" -delete 	&& apt-get update && apt-get install -y binutils && rm -rf /var/lib/apt/lists/* 	&& { find /usr/local/mysql -type f -executable -exec strip --strip-all '{}' + || true; } 	&& apt-get purge -y --auto-remove binutils
# Wed, 14 Dec 2016 02:49:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/mysql/bin:/usr/local/mysql/scripts
# Wed, 14 Dec 2016 02:49:51 GMT
RUN mkdir -p /etc/mysql/conf.d 	&& { 		echo '[mysqld]'; 		echo 'skip-host-cache'; 		echo 'skip-name-resolve'; 		echo 'datadir = /var/lib/mysql'; 		echo '!includedir /etc/mysql/conf.d/'; 	} > /etc/mysql/my.cnf
# Wed, 14 Dec 2016 02:49:52 GMT
RUN mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 14 Dec 2016 02:49:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Dec 2016 02:49:53 GMT
COPY file:245ce9bcff8bc17aee3109b8f5b96ad95b196827b76edea92605d4b60dfbe885 in /usr/local/bin/ 
# Wed, 14 Dec 2016 02:49:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Dec 2016 02:50:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Dec 2016 02:50:05 GMT
EXPOSE 3306/tcp
# Wed, 14 Dec 2016 02:50:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d5846e536af54d4f4773fb5173c759fb8b3673a34710a7e1fe15b4120dc8d2`  
		Last Modified: Wed, 14 Dec 2016 03:24:37 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e9152a1702d9b527b4e753786743d20ceea693424429f5da60410d7b02ddf`  
		Last Modified: Wed, 14 Dec 2016 03:24:36 GMT  
		Size: 1.2 MB (1216944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832e6b0304969b9baa6a38a8e32da0aaf7d7cbf9476c31d006f335264edc6147`  
		Last Modified: Wed, 14 Dec 2016 01:03:50 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a553059860edcfc86f7cd3be7dc60f24b7f6bd15dfc1974520d7b6f3519b2d13`  
		Last Modified: Wed, 14 Dec 2016 03:32:04 GMT  
		Size: 8.2 MB (8220200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463fe937682a93015a683a066d1a056ced8186669e7df5fdcc65e042b25fb0ae`  
		Last Modified: Wed, 14 Dec 2016 03:31:57 GMT  
		Size: 101.2 KB (101160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5052b27ac6c0eaeafc660eadc2fe5914061a0d103d19e25afa0d103ceb6cc560`  
		Last Modified: Wed, 14 Dec 2016 03:32:04 GMT  
		Size: 26.5 MB (26508378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c43a1d263b4fc6dec3ce87a0c0fcd935f5dd48746b29c575f1645b2fa3f719`  
		Last Modified: Wed, 14 Dec 2016 03:31:55 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89e353685e430a7abb936915c30b76a24cfcfa6a455c509b616ab66fe3a39f8`  
		Last Modified: Wed, 14 Dec 2016 03:31:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861de1bba8fae0bbb6f6cb48fcd8e11c1a45c2c28f3aae1abe093171a742875e`  
		Last Modified: Wed, 14 Dec 2016 03:31:54 GMT  
		Size: 2.2 KB (2209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6924d5ac023a15413396f32732695f634d16bdd0b95a352a0a8d4d560530e1`  
		Last Modified: Wed, 14 Dec 2016 03:31:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.5`

```console
$ docker pull mysql@sha256:7af3fe3e7e2dc23df2768eb340fc656af145f48efd0137113a435606566344d3
```

-	Platforms:
	-	linux; amd64

### `mysql:5.5` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87414704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8cd588fa9c6441f682393dd9f200046c28d176d524c11979ec64d81261fd59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Wed, 14 Dec 2016 01:00:10 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Dec 2016 01:00:11 GMT
ENV GOSU_VERSION=1.7
# Wed, 14 Dec 2016 01:00:29 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Wed, 14 Dec 2016 01:00:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Dec 2016 02:48:34 GMT
RUN apt-get update && apt-get install -y perl --no-install-recommends && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 02:48:41 GMT
RUN apt-get update && apt-get install -y libaio1 pwgen && rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2016 02:48:50 GMT
ENV MYSQL_MAJOR=5.5
# Wed, 14 Dec 2016 02:48:50 GMT
ENV MYSQL_VERSION=5.5.54
# Wed, 14 Dec 2016 02:49:40 GMT
RUN apt-get update && apt-get install -y ca-certificates wget --no-install-recommends && rm -rf /var/lib/apt/lists/* 	&& wget "https://cdn.mysql.com/Downloads/MySQL-$MYSQL_MAJOR/mysql-$MYSQL_VERSION-linux2.6-x86_64.tar.gz" -O mysql.tar.gz 	&& wget "https://cdn.mysql.com/Downloads/MySQL-$MYSQL_MAJOR/mysql-$MYSQL_VERSION-linux2.6-x86_64.tar.gz.asc" -O mysql.tar.gz.asc 	&& apt-get purge -y --auto-remove ca-certificates wget 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys A4A9406876FCBD3C456770C88C718D3B5072E1F5 	&& gpg --batch --verify mysql.tar.gz.asc mysql.tar.gz 	&& rm -r "$GNUPGHOME" mysql.tar.gz.asc 	&& mkdir /usr/local/mysql 	&& tar -xzf mysql.tar.gz -C /usr/local/mysql --strip-components=1 	&& rm mysql.tar.gz 	&& rm -rf /usr/local/mysql/mysql-test /usr/local/mysql/sql-bench 	&& rm -rf /usr/local/mysql/bin/*-debug /usr/local/mysql/bin/*_embedded 	&& find /usr/local/mysql -type f -name "*.a" -delete 	&& apt-get update && apt-get install -y binutils && rm -rf /var/lib/apt/lists/* 	&& { find /usr/local/mysql -type f -executable -exec strip --strip-all '{}' + || true; } 	&& apt-get purge -y --auto-remove binutils
# Wed, 14 Dec 2016 02:49:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/mysql/bin:/usr/local/mysql/scripts
# Wed, 14 Dec 2016 02:49:51 GMT
RUN mkdir -p /etc/mysql/conf.d 	&& { 		echo '[mysqld]'; 		echo 'skip-host-cache'; 		echo 'skip-name-resolve'; 		echo 'datadir = /var/lib/mysql'; 		echo '!includedir /etc/mysql/conf.d/'; 	} > /etc/mysql/my.cnf
# Wed, 14 Dec 2016 02:49:52 GMT
RUN mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Wed, 14 Dec 2016 02:49:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Dec 2016 02:49:53 GMT
COPY file:245ce9bcff8bc17aee3109b8f5b96ad95b196827b76edea92605d4b60dfbe885 in /usr/local/bin/ 
# Wed, 14 Dec 2016 02:49:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 14 Dec 2016 02:50:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Dec 2016 02:50:05 GMT
EXPOSE 3306/tcp
# Wed, 14 Dec 2016 02:50:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d5846e536af54d4f4773fb5173c759fb8b3673a34710a7e1fe15b4120dc8d2`  
		Last Modified: Wed, 14 Dec 2016 03:24:37 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e9152a1702d9b527b4e753786743d20ceea693424429f5da60410d7b02ddf`  
		Last Modified: Wed, 14 Dec 2016 03:24:36 GMT  
		Size: 1.2 MB (1216944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832e6b0304969b9baa6a38a8e32da0aaf7d7cbf9476c31d006f335264edc6147`  
		Last Modified: Wed, 14 Dec 2016 01:03:50 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a553059860edcfc86f7cd3be7dc60f24b7f6bd15dfc1974520d7b6f3519b2d13`  
		Last Modified: Wed, 14 Dec 2016 03:32:04 GMT  
		Size: 8.2 MB (8220200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463fe937682a93015a683a066d1a056ced8186669e7df5fdcc65e042b25fb0ae`  
		Last Modified: Wed, 14 Dec 2016 03:31:57 GMT  
		Size: 101.2 KB (101160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5052b27ac6c0eaeafc660eadc2fe5914061a0d103d19e25afa0d103ceb6cc560`  
		Last Modified: Wed, 14 Dec 2016 03:32:04 GMT  
		Size: 26.5 MB (26508378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c43a1d263b4fc6dec3ce87a0c0fcd935f5dd48746b29c575f1645b2fa3f719`  
		Last Modified: Wed, 14 Dec 2016 03:31:55 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89e353685e430a7abb936915c30b76a24cfcfa6a455c509b616ab66fe3a39f8`  
		Last Modified: Wed, 14 Dec 2016 03:31:54 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861de1bba8fae0bbb6f6cb48fcd8e11c1a45c2c28f3aae1abe093171a742875e`  
		Last Modified: Wed, 14 Dec 2016 03:31:54 GMT  
		Size: 2.2 KB (2209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6924d5ac023a15413396f32732695f634d16bdd0b95a352a0a8d4d560530e1`  
		Last Modified: Wed, 14 Dec 2016 03:31:54 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
