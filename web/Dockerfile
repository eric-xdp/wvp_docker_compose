FROM nginx:latest
# 定义作者
MAINTAINER ericxu

#删除目录下的default.conf文件
#RUN rm /etc/nginx/conf.d/default.conf
#设置时区
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone

#将本地nginx.conf配置覆盖nginx配置
COPY nginx.conf /etc/nginx/nginx.conf
# 将vue编译好的dist文件中的内容复制到 /usr/share/nginx/html/ 这个目录下面
COPY static/  /usr/share/nginx/html/
#声名端口
EXPOSE 80

RUN echo 'web project build success!!'
