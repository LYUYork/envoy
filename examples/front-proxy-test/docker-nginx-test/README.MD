

reference: https://blog.csdn.net/qq_38637558/article/details/104395561

docker run --name nginx -d -p 80:80 --restart=always --privileged=true --net=host -v /docker/nginx/html:/usr/share/nginx/html -v /docker/nginx/conf/nginx.conf:/etc/nginx/nginx.conf  -v /docker/nginx/logs:/var/log/nginx -v /docker/nginx/conf.d:/etc/nginx/conf.d -d nginx

docker run  -d -p 80:80  \
  -v /workspace/envoy/examples/front-proxy-test/docker-nginx-test/nginx/html:/usr/share/nginx/html \
  -v /workspace/envoy/examples/front-proxy-test/docker-nginx-test/nginx/conf/nginx.conf:/etc/nginx/nginx.conf  \
  -v /workspace/envoy/examples/front-proxy-test/docker-nginx-test/nginx/logs:/var/log/nginx \
  -v /workspace/envoy/examples/front-proxy-test/docker-nginx-test/nginx/conf.d:/etc/nginx/conf.d  nginx
