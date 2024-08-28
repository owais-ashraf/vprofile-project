FROM mysql:8.0.33   
LABEL "Project"="ProfileApp"
LABEL "Author"="Owais" 

ARG MYSQL_ROOT_PASSWORD=sqlpass
ENV MYSQL_DATABASE="accounts"
COPY db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql


