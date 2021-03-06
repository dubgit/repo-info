## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:8afe60eceefef9f43909c83204597c19aaede91a84637a36272c41d634326c2f
```

-	Platforms:
	-	linux; amd64

### `neo4j:enterprise` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131264526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f7b98e12141e333211b0360ebe57ff119ed7566261ed0bfef728f5c3878c2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 18 Oct 2016 20:31:22 GMT
ADD file:7afbc23fda8b0b3872623c16af8e3490b2cee951aed14b3794389c2f946cc8c7 in / 
# Tue, 18 Oct 2016 20:39:57 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2016 20:39:58 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 18 Oct 2016 20:40:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Tue, 18 Oct 2016 20:40:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 17 Nov 2016 21:47:51 GMT
ENV JAVA_VERSION=8u111
# Thu, 17 Nov 2016 21:47:52 GMT
ENV JAVA_ALPINE_VERSION=8.111.14-r0
# Thu, 17 Nov 2016 21:47:57 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 09 Dec 2016 17:57:16 GMT
RUN apk add --no-cache --quiet     bash     curl
# Fri, 09 Dec 2016 17:57:37 GMT
ENV NEO4J_SHA256=1f289296c23004ace4d37e14f2af433d203dfb028977534429e766bc308d584a
# Fri, 09 Dec 2016 17:57:37 GMT
ENV NEO4J_TARBALL=neo4j-enterprise-3.1.0-unix.tar.gz
# Fri, 09 Dec 2016 17:57:38 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.1.0-unix.tar.gz
# Fri, 09 Dec 2016 17:57:38 GMT
COPY file:2e411d607fa15f91ae6f4b515dde6bf3e158d34c0036556e00553ed1c50cd63d in /tmp/ 
# Fri, 09 Dec 2016 17:57:54 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.1.0-unix.tar.gz
RUN curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -csw -     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* /var/lib/neo4j     && rm ${NEO4J_TARBALL}
# Fri, 09 Dec 2016 17:57:54 GMT
WORKDIR /var/lib/neo4j
# Fri, 09 Dec 2016 17:57:55 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.1.0-unix.tar.gz
RUN mv data /data     && ln -s /data
# Fri, 09 Dec 2016 17:57:56 GMT
VOLUME [/data]
# Fri, 09 Dec 2016 17:57:57 GMT
COPY file:77937095ede0ebf8d922e2d061f12dc5de64a045c38a47b59579caac7c90f6f6 in /docker-entrypoint.sh 
# Fri, 09 Dec 2016 17:57:57 GMT
EXPOSE 7473/tcp 7474/tcp 7687/tcp
# Fri, 09 Dec 2016 17:58:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Dec 2016 17:58:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3690ec4760f95690944da86dc4496148a63d85c9e3100669a318110092f6862f`  
		Last Modified: Tue, 18 Oct 2016 20:32:39 GMT  
		Size: 2.3 MB (2312958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdb77eb56b4c44907a822ccdf607323c1f42fd024b7db6be146dd049d95f305`  
		Last Modified: Tue, 18 Oct 2016 20:45:34 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857cbad9cd9a8609720fe041554046e94f0813b64887c3c06eac0c2cfb2be741`  
		Last Modified: Thu, 17 Nov 2016 22:03:51 GMT  
		Size: 39.7 MB (39670171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b62786ec2d3bc148f86b75dd76dbcc0ad7911b52f4ab423e74b1da54578148`  
		Last Modified: Fri, 09 Dec 2016 17:58:26 GMT  
		Size: 1.5 MB (1455365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b42f58e6fa91684d74c13fddee0d9f725e1d8c4e7d3cf8c634532ac44bdfcef`  
		Last Modified: Fri, 09 Dec 2016 17:59:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5065533ca78f25f42d5804ab61da94918b0bde5444599e5ad4321fbee438cc08`  
		Last Modified: Fri, 09 Dec 2016 17:59:36 GMT  
		Size: 87.8 MB (87824258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b4708f9ffbf302db484ee286b5ca7c6b1b71836f711c7fdbe703209c680b93`  
		Last Modified: Fri, 09 Dec 2016 17:59:28 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c73aa33248f884d67d47f698793ec4b38f16ee3385d2e99c9d7e8a898bae0a`  
		Last Modified: Fri, 09 Dec 2016 17:59:28 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
