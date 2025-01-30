FROM apache/superset:latest

USER root

RUN apt update && apt install libpq-dev gcc -y

ENV ADMIN_USERNAME $ADMIN_USERNAME
ENV ADMIN_EMAIL $ADMIN_EMAIL
ENV ADMIN_PASSWORD $ADMIN_PASSWORD

COPY --chown=superset:superset --chmod=755 ./superset-init.sh /

RUN pip install psycopg2

## superset ayar dosyasının kopyalanması
COPY superset_config.py /app/
ENV SUPERSET_CONFIG_PATH /app/superset_config.py

USER superset

ENTRYPOINT [ "/superset-init.sh" ]
