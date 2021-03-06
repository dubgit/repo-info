## `iojs:2-onbuild`

```console
$ docker pull iojs@sha256:d768014b8702dd0c4367b70a28d0f14048e22a8a2a685b054878f4b3e948337a
```

-	Platforms:
	-	linux; amd64

### `iojs:2-onbuild` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.5 MB (251539485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c803c57eef424858e6b77db7c1c9f109b2349693bd5eafbadb14537f6e01d2`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 13 Dec 2016 22:10:59 GMT
ADD file:1d214d2782eaccc743b8d683ccecf2f87f12a0ecdfbcd6fdf4943ce616f23870 in / 
# Tue, 13 Dec 2016 22:10:59 GMT
CMD ["/bin/bash"]
# Tue, 13 Dec 2016 23:00:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:00:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Dec 2016 18:59:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Dec 2016 02:30:37 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     0034A06D9D9B0064CE8ADF6BF1747F4AD2306D93     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"   ; done
# Fri, 16 Dec 2016 02:30:37 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Fri, 16 Dec 2016 02:30:45 GMT
ENV IOJS_VERSION=2.5.0
# Fri, 16 Dec 2016 02:30:49 GMT
RUN curl -SLO "https://iojs.org/dist/v$IOJS_VERSION/iojs-v$IOJS_VERSION-linux-x64.tar.gz"   && curl -SLO "https://iojs.org/dist/v$IOJS_VERSION/SHASUMS256.txt.asc"   && gpg --verify SHASUMS256.txt.asc   && grep " iojs-v$IOJS_VERSION-linux-x64.tar.gz\$" SHASUMS256.txt.asc | sha256sum -c -   && tar -xzf "iojs-v$IOJS_VERSION-linux-x64.tar.gz" -C /usr/local --strip-components=1   && rm "iojs-v$IOJS_VERSION-linux-x64.tar.gz" SHASUMS256.txt.asc
# Fri, 16 Dec 2016 02:30:49 GMT
CMD ["iojs"]
# Fri, 16 Dec 2016 02:30:50 GMT
RUN mkdir -p /usr/src/app
# Fri, 16 Dec 2016 02:30:51 GMT
WORKDIR /usr/src/app
# Fri, 16 Dec 2016 02:30:51 GMT
ONBUILD COPY package.json /usr/src/app/
# Fri, 16 Dec 2016 02:30:51 GMT
ONBUILD RUN npm install
# Fri, 16 Dec 2016 02:30:51 GMT
ONBUILD COPY . /usr/src/app
# Fri, 16 Dec 2016 02:30:52 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:75a822cd7888e394c49828b951061402d31745f596b1f502758570f2d0ee79e2`  
		Last Modified: Tue, 13 Dec 2016 22:16:41 GMT  
		Size: 51.4 MB (51363125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57de64c72267e88e952b064236cb906c7626f7c07a1a2d5900cf6953e72632b3`  
		Last Modified: Wed, 14 Dec 2016 03:04:38 GMT  
		Size: 18.5 MB (18529983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4306be1e8943b446026b96c2ef7b3ab8471c760774fd1cd11334df7084fed57b`  
		Last Modified: Wed, 14 Dec 2016 03:04:50 GMT  
		Size: 42.5 MB (42502002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871436ab7225503e9e951a7acb7b1689a91a60d033bf8cbabcd40fe5ca4cfc87`  
		Last Modified: Thu, 15 Dec 2016 19:33:52 GMT  
		Size: 129.8 MB (129823619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01833a8a4de60065559665201eb240243591860b460e80a2415f412562d428ae`  
		Last Modified: Mon, 19 Dec 2016 22:51:29 GMT  
		Size: 69.4 KB (69385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa03d1f37854f0c41096156bfd90a62c3aefda351ff3a554bd88578eba36f6b`  
		Last Modified: Mon, 19 Dec 2016 22:54:27 GMT  
		Size: 9.3 MB (9251244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd5c9413ebd7a3baaba8d0fa04ad26160ceca4ef24a6a6df65e71059e77a62d`  
		Last Modified: Mon, 19 Dec 2016 22:55:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
