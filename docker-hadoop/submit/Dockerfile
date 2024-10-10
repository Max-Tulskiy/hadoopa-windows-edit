FROM maxtulskiy/haboop-base-image:latest

COPY WordCount.jar /opt/hadoop/applications/WordCount.jar

ENV JAR_FILEPATH="/opt/hadoop/applications/WordCount.jar"
ENV CLASS_TO_RUN="WordCount"
ENV PARAMS="/input /output"

ADD run.sh /run.sh

RUN apt-get update && apt-get install -y dos2unix
RUN dos2unix /run.sh

RUN chmod a+x /run.sh

CMD ["/run.sh"]
