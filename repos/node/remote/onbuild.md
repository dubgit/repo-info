## `node:onbuild`

```console
$ docker pull node@sha256:d20f0465e1271c5fa702cda79f4aae8f6b15c3f136b949adaa914279be3c22bd
```

-	Platforms:
	-	linux; amd64

### `node:onbuild` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257685841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3ae1917fbd0360703637a185b335c1beda9a4d8fc0ba49c1ce7843a5e8a25f`
-	Default Command: `["npm","start"]`

```dockerfile
# Mon, 07 Nov 2016 20:30:25 GMT
ADD file:41ea5187c50116884c38d9ec51d920d79cfaeb2a61c52e07a97f457419a10a4f in / 
# Mon, 07 Nov 2016 20:30:26 GMT
CMD ["/bin/bash"]
# Mon, 07 Nov 2016 22:27:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2016 22:27:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2016 22:28:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libncurses-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Wed, 23 Nov 2016 19:04:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 23 Nov 2016 19:04:51 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     0034A06D9D9B0064CE8ADF6BF1747F4AD2306D93     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     B9AE9905FFD7803F25714661B63B535A4C206CA9     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key";   done
# Wed, 23 Nov 2016 19:04:51 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Wed, 07 Dec 2016 22:53:55 GMT
ENV NODE_VERSION=7.2.1
# Wed, 07 Dec 2016 22:54:00 GMT
RUN curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.xz"   && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-x64.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-x64.tar.xz" -C /usr/local --strip-components=1   && rm "node-v$NODE_VERSION-linux-x64.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 07 Dec 2016 22:54:01 GMT
CMD ["node"]
# Wed, 07 Dec 2016 23:10:46 GMT
RUN mkdir -p /usr/src/app
# Wed, 07 Dec 2016 23:10:46 GMT
WORKDIR /usr/src/app
# Wed, 07 Dec 2016 23:10:47 GMT
ONBUILD ARG NODE_ENV
# Wed, 07 Dec 2016 23:10:47 GMT
ONBUILD ENV NODE_ENV $NODE_ENV
# Wed, 07 Dec 2016 23:10:47 GMT
ONBUILD COPY package.json /usr/src/app/
# Wed, 07 Dec 2016 23:10:48 GMT
ONBUILD RUN npm install
# Wed, 07 Dec 2016 23:10:48 GMT
ONBUILD COPY . /usr/src/app
# Wed, 07 Dec 2016 23:10:49 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:386a066cd84a33a04d560c42bef66d1dd64ebfc76de78550e5fd0f8d57778bca`  
		Last Modified: Mon, 07 Nov 2016 20:34:04 GMT  
		Size: 51.4 MB (51356989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ea8418708338e40dce9179cfe97fd116831f1601be50fef48ea6011653c986`  
		Last Modified: Mon, 07 Nov 2016 22:57:05 GMT  
		Size: 18.5 MB (18528477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b459c9f665cc39ff5fc09071b5dada4dad766573d962276f999d0c466d5405`  
		Last Modified: Mon, 07 Nov 2016 22:57:53 GMT  
		Size: 42.5 MB (42498243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3ee139a57774dc3728a4bf9675bc379458093585e42f384852e644b1b272ac`  
		Last Modified: Mon, 07 Nov 2016 22:59:05 GMT  
		Size: 129.8 MB (129808774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78ff7d0315bea8f26f4cd551b1ef5d35a665e285b8b838c10df6ec733a30749`  
		Last Modified: Wed, 23 Nov 2016 19:42:29 GMT  
		Size: 4.4 KB (4364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ba677961ff50e4aba3f7fd2e433b25fc9f1d4367c6e140fdbb397edbf0c1e5`  
		Last Modified: Wed, 23 Nov 2016 19:42:28 GMT  
		Size: 97.2 KB (97218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2022c49e66ec94fec2f4c01bcb640ac6d26bb4885720d5924650a4b13cd8be`  
		Last Modified: Wed, 07 Dec 2016 23:21:45 GMT  
		Size: 15.4 MB (15391650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445250e8a94b8e8014ab37ac5686991f9232e96793218b871744806dde2c583b`  
		Last Modified: Wed, 07 Dec 2016 23:24:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
