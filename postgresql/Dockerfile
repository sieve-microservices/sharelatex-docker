FROM mic92/sharelatex-base

VOLUME /data/db
RUN apt install -y postgresql

ENV PG_VERSION="9.3" \
    PGDATA="/var/lib/postgresql/data"
VOLUME ["/var/lib/postgresql/data"]
RUN chown postgres $PGDATA
EXPOSE 5432
ENTRYPOINT ["entrypoint"]
ADD entrypoint /usr/local/bin/entrypoint
CMD ["postgres"]
