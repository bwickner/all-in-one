# syntax=docker/dockerfile:latest
# From https://github.com/ONLYOFFICE/Docker-DocumentServer/blob/master/Dockerfile
FROM onlyoffice/documentserver:9.0.3.1

# USER root is probably used

COPY --chmod=775 healthcheck.sh /healthcheck.sh

HEALTHCHECK --start-period=60s --retries=9 CMD /healthcheck.sh
LABEL com.centurylinklabs.watchtower.enable="false" \
    org.label-schema.vendor="Nextcloud"
