FROM openjdk:8u131-jre-alpine
MAINTAINER zhouyq@goodrain.com

# china repositories mirror
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories

# modify timezone and install the necessary software
RUN apk add --no-cache tzdata libc6-compat libstdc++ tar sed wget curl bash su-exec netcat-openbsd && \
       sed -i -e "s/bin\/ash/bin\/bash/" /etc/passwd && \
       ln -s /lib /lib64 && \
       cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
       echo "Asia/Shanghai" >  /etc/timezone && \
       date && apk del --no-cache tzdata && \
       sed -i -r 's#^(securerandom.source)=.*#\1=file:/dev/./urandom/#' $JAVA_HOME/lib/security/java.security

ENV LANG en_US.utf8
