FROM maxtulskiy/hadoop-base-image:latest

HEALTHCHECK CMD curl -f http://localhost:8042/ || exit 1

ADD run.sh /run.sh

RUN apt-get update && apt-get install -y dos2unix
RUN dos2unix /run.sh

RUN chmod a+x /run.sh

EXPOSE 8042

CMD ["/run.sh"]
