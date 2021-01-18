FROM alpine:3.12

#ENV USER=nas
#ENV GROUP=smbgrp
#ENV UID=1000
#ENV GID=1001

RUN apk add --update \
    samba-common-tools \
#    samba-client \
    samba-server \
    && rm -rf /var/cache/apk/*

#RUN addgroup\
#     --gid "$GID" \
#     "$GROUP" && \
#    adduser \
#    --disabled-password \
#    --gecos "" \
#    --home "$(pwd)" \
#    --ingroup "$GROUP" \
#    --ingroup root \
#    --no-create-home \
#    --uid "$UID" \
#    "$USER"

#RUN groupadd -g 1001 smbgrp && \
#    useradd -r -u 9009 -g smbgrp nas

#USER "$USER"

VOLUME ["/etc", "/var/cache/samba", "/var/lib/samba", "/var/log/samba",\
        "/run/samba"]

ENTRYPOINT ["smbd", "--foreground", "--log-stdout", "--no-process-group"]
CMD []