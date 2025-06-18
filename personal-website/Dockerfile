# 使用轻量级Nginx镜像
FROM nginx:alpine

# 删除默认欢迎页面
RUN rm /usr/share/nginx/html/*

# 复制网站文件
COPY index.html /usr/share/nginx/html/
COPY style.css /usr/share/nginx/html/
COPY Tangziyu20232046.jpg /usr/share/nginx/html/

# 优化Nginx配置
RUN echo "server_tokens off;" > /etc/nginx/conf.d/security.conf

# 暴露80端口
EXPOSE 80

# 启动Nginx
CMD ["nginx", "-g", "daemon off;"]