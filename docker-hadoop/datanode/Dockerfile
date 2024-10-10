FROM maxtulskiy/hadoop-base-image:latest

HEALTHCHECK CMD curl -f http://localhost:9864/ || exit 1

ENV HDFS_CONF_dfs_datanode_data_dir=file:///hadoop/dfs/data
RUN mkdir -p /hadoop/dfs/data
VOLUME /hadoop/dfs/data

ADD run.sh /run.sh

RUN apt-get update && apt-get install -y dos2unix
RUN dos2unix /run.sh

RUN chmod a+x /run.sh

EXPOSE 9864

CMD ["/run.sh"]
