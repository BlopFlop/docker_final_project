FROM postgres:17-alpine
COPY init.sql /docker-entrypoint-initdb.d/
HEALTHCHECK --interval=10s --timeout=5s --start-period=30s --retries=5 \
    CMD pg_isready -U ${POSTGRES_USER} -d ${POSTGRES_DB} || exit 1