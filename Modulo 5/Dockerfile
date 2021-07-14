FROM nginx
RUN useradd natalia
COPY index.html  /usr/share/nginx/html
ENV archivo docker
WORKDIR /usr/share/nginx/html
RUN echo "$archivo"  >  /usr/share/nginx/html/env.html
EXPOSE 90
LABEL version = 1
USER natalia 
RUN echo  "Yo soy ${whoami}" > /tmp/yo.html
USER root
RUN cp /tmp/yo.html /usr/share/nginx/html/docker.html
VOLUME /var/log/nginx