## `tomcat:jre8-alpine`

```console
$ docker pull tomcat@sha256:6f2772f06dbd34f5b8950271b70d8e8b62395961df4128bd00fcd2093ab7020b
```

-	Platforms:
	-	linux; amd64

### `tomcat:jre8-alpine` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56759843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cc7d10e9ddbcf08068fcc223fa5a0ba888a5978349863ed840eda0e35b4797`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 29 Aug 2016 23:49:14 GMT
ADD file:852e9d0cb9d906535af512a89339fc70b2873a0f94defbcbe41cd44942dd6ac8 in / 
# Tue, 30 Aug 2016 19:53:16 GMT
ENV LANG=C.UTF-8
# Tue, 30 Aug 2016 19:53:17 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 30 Aug 2016 19:56:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Tue, 30 Aug 2016 19:56:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Tue, 30 Aug 2016 19:56:05 GMT
ENV JAVA_VERSION=8u92
# Tue, 30 Aug 2016 19:56:05 GMT
ENV JAVA_ALPINE_VERSION=8.92.14-r1
# Tue, 30 Aug 2016 19:56:10 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 31 Aug 2016 04:28:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 31 Aug 2016 04:28:10 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Wed, 31 Aug 2016 04:28:11 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 31 Aug 2016 04:28:11 GMT
WORKDIR /usr/local/tomcat
# Wed, 31 Aug 2016 04:28:11 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 31 Aug 2016 04:28:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 31 Aug 2016 04:28:17 GMT
RUN apk add --no-cache gnupg
# Wed, 31 Aug 2016 04:28:34 GMT
RUN set -ex 	&& for key in 		05AB33110949707C93A279E3D3EFE6B686867BA6 		07E48665A34DCAFAE522E5E6266191C37C037D42 		47309207D818FFD8DCD3F83F1931D684307A10A5 		541FBE7D8F78B25E055DDEE13C370389288584E7 		61B832AC2F1C5A90F0F9B00A1C506407564C17A3 		713DA88BE50911535FE716F5208B0AB1D63011C7 		79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 		9BA44C2621385CB966EBA586F72C284D731FABEE 		A27677289986DB50844682F8ACB77FC2E86E29AC 		A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 		DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 		F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE 		F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23 	; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Wed, 31 Aug 2016 04:31:44 GMT
ENV TOMCAT_MAJOR=8
# Wed, 07 Sep 2016 19:20:09 GMT
ENV TOMCAT_VERSION=8.0.37
# Wed, 07 Sep 2016 19:20:09 GMT
ENV TOMCAT_TGZ_URL=https://www.apache.org/dist/tomcat/tomcat-8/v8.0.37/bin/apache-tomcat-8.0.37.tar.gz
# Wed, 07 Sep 2016 19:20:20 GMT
RUN set -x 		&& apk add --no-cache --virtual .fetch-deps 		ca-certificates 		tar 		openssl 	&& wget -O tomcat.tar.gz "$TOMCAT_TGZ_URL" 	&& wget -O tomcat.tar.gz.asc "$TOMCAT_TGZ_URL.asc" 	&& gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz 	&& tar -xvf tomcat.tar.gz --strip-components=1 	&& rm bin/*.bat 	&& rm tomcat.tar.gz* 		&& nativeBuildDir="$(mktemp -d)" 	&& tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1 	&& apk add --no-cache --virtual .native-build-deps 		apr-dev 		gcc 		libc-dev 		make 		"openjdk${JAVA_VERSION%%[-~bu]*}"="$JAVA_ALPINE_VERSION" 		openssl-dev 	&& ( 		export CATALINA_HOME="$PWD" 		&& cd "$nativeBuildDir/native" 		&& ./configure 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes 		&& make -j$(getconf _NPROCESSORS_ONLN) 		&& make install 	) 	&& runDeps="$( 		scanelf --needed --nobanner --recursive "$TOMCAT_NATIVE_LIBDIR" 			| awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }' 			| sort -u 			| xargs -r apk info --installed 			| sort -u 	)" 	&& apk add --virtual .tomcat-native-rundeps $runDeps 	&& apk del .fetch-deps .native-build-deps 	&& rm -rf "$nativeBuildDir" 	&& rm bin/tomcat-native.tar.gz
# Wed, 07 Sep 2016 19:20:27 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 07 Sep 2016 19:20:27 GMT
EXPOSE 8080/tcp
# Wed, 07 Sep 2016 19:20:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e110a4a1794126ef308a49f2d65785af2f25538f06700721aad8283b81fdfa58`  
		Last Modified: Thu, 23 Jun 2016 19:56:16 GMT  
		Size: 2.3 MB (2310286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a696cba1f6e865421664a7bf9bf585bcfaa924d56b7d2a112a799e00a7433791`  
		Last Modified: Tue, 30 Aug 2016 21:11:27 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc427bd93e958b2f8b2cadc810c692edbba6856a8ff08434066b43be35ec6b68`  
		Last Modified: Tue, 30 Aug 2016 21:11:37 GMT  
		Size: 39.6 MB (39647584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af85cd158be3d3090154203fe6d77249ddbe712b5555632358a7f8286f9e0dbf`  
		Last Modified: Wed, 31 Aug 2016 21:54:21 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce29bb07b265e57baad737c19907385ee643ef88829fcff9916a85016ae9a21`  
		Last Modified: Wed, 31 Aug 2016 21:54:24 GMT  
		Size: 4.0 MB (3985954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8696de1a069a132515efd7a75442792c14dc22945baac43bba0cc2eda5c94042`  
		Last Modified: Wed, 31 Aug 2016 21:54:21 GMT  
		Size: 105.6 KB (105641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c96129829f453b0e98b0d78a24d49cccc2c686d2e603027b005a0c94b7cbabb`  
		Last Modified: Wed, 07 Sep 2016 19:29:20 GMT  
		Size: 10.7 MB (10709881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a3d104d9667bce2d2256528a77213158b30381d6f1cd9148eb0f5cd4d710d4`  
		Last Modified: Wed, 07 Sep 2016 19:29:17 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip