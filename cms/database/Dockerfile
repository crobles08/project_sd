FROM mysql:8.0.37
ENV MYSQL_ROOT_PASSWORD=secret
ENV MYSQL_DATABASE=wordpress
COPY bd_vshowcase.sql /docker-entrypoint-initdb.d/
EXPOSE 3306
