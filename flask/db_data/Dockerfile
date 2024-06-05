FROM mysql:8.0.37
ENV MYSQL_ROOT_PASSWORD=1234
ENV MYSQL_DATABASE=municipios
COPY municipios.sql /docker-entrypoint-initdb.d/
EXPOSE 3306
