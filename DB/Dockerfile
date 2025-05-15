FROM mysql:latest

LABEL database="studentapp"

# Environment variables for MySQL image
ENV MYSQL_ROOT_PASSWORD=admin123 \
    MYSQL_USER=admin \
    MYSQL_PASSWORD=admin123 \
    MYSQL_DATABASE=studentapp
    ENDPOINT=database-1.cd484qi6woeo.ap-northeast-2.rds.amazonaws.com

# Initialization script
COPY init-db.sql /docker-entrypoint-initdb.d/

# Expose MySQL port
EXPOSE 3306

# Start the MySQL server (handled by base image)
CMD ["mysqld"]
