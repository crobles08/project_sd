FROM python:3.12.3-alpine3.18

# Instalar dependencias
RUN apk update && \
    apk add --no-cache pkgconfig mariadb-dev build-base && \
    apk add --no-cache python3-dev py3-pip && \
    pip install --upgrade pip && \
    pip install virtualenv && \
    rm -rf /var/cache/apk/*

# Establecer el directorio de trabajo
WORKDIR /app

# Copiar el código de la aplicación
COPY ./app .

# Crear un entorno virtual e instalar dependencias de Python
RUN virtualenv venv && \
    /bin/sh -c "source venv/bin/activate && pip install --no-cache-dir -r requirements.txt"

# Establecer permisos
RUN chmod -R 777 /app

# Comando para ejecutar la aplicación
CMD ["/bin/sh", "-c", "source venv/bin/activate && flask run --host=0.0.0.0"]
