## `openjdk:9-jdk`

```console
$ docker pull openjdk@sha256:9bcef066dc6e6fe791b5ec8c610054e482c156add6d24a7b44556a100ff77ce4
```

-	Platforms:
	-	linux; amd64

### `openjdk:9-jdk` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260942906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1800de06a3eb5377236406c5fdd3d74417a1799b2152cef43334553153735620`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Dec 2016 22:12:19 GMT
ADD file:1ec9813ae98ad32fbb472ab2d0a10bfffc02970b272ce3595007bf94381ea99d in / 
# Tue, 13 Dec 2016 22:12:20 GMT
CMD ["/bin/bash"]
# Tue, 13 Dec 2016 23:00:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:01:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:55:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Dec 2016 23:55:38 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Tue, 13 Dec 2016 23:55:38 GMT
ENV LANG=C.UTF-8
# Tue, 13 Dec 2016 23:55:39 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 13 Dec 2016 23:55:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-9-openjdk-amd64
# Mon, 19 Dec 2016 21:07:42 GMT
ENV JAVA_VERSION=9~b149
# Mon, 19 Dec 2016 21:07:42 GMT
ENV JAVA_DEBIAN_VERSION=9~b149-1
# Mon, 19 Dec 2016 21:08:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	&& rm -rf /var/lib/apt/lists/* 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
```

-	Layers:
	-	`sha256:96adffeba9716172608de9e458530715467b8d8a3d22b249de6f7d2f0c6e9f55`  
		Last Modified: Tue, 13 Dec 2016 22:20:27 GMT  
		Size: 43.9 MB (43866938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72591232915f25a33b2dcf0ed9fea09256ec5c0988bce2e515b6e9911274adc`  
		Last Modified: Wed, 14 Dec 2016 03:20:29 GMT  
		Size: 20.9 MB (20945421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e5ec7de751dd011b9b64ec0ee93775040bb91451b2b1dc95ec4a175de462c3`  
		Last Modified: Wed, 14 Dec 2016 03:20:43 GMT  
		Size: 51.2 MB (51219215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121993890cd4b642ee91546b2c0b7c655abd4287f759bed0220f854f61d6608f`  
		Last Modified: Wed, 14 Dec 2016 03:20:20 GMT  
		Size: 648.4 KB (648436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c137dfeb464dfb54e087d20ccb9a6525a515aab6121f1184499fa1b539667d7`  
		Last Modified: Wed, 14 Dec 2016 03:20:23 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6d48ce44eb06a1b268d4330e98380ab8ff70b3b5f746a1db08d33da596f50e`  
		Last Modified: Wed, 14 Dec 2016 03:20:19 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff400272ea3d118646477c1fe56f335cbaa29869ad52808235f3293ab7b7a29a`  
		Last Modified: Mon, 19 Dec 2016 21:27:07 GMT  
		Size: 144.3 MB (144262440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
