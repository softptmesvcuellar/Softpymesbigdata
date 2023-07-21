FROM hadoop-hive-spark-base

ENV DATADIR=/opt/hadoop/dfs/data
RUN mkdir -p /opt/hadoop/dfs/data
VOLUME /opt/hadoop/dfs/data

ENV SPARK_PUBLIC_DNS=localhost
ENV SPARK_MASTER_ADDRESS=spark://master:7077

COPY run.sh /usr/local/sbin/
RUN sudo chmod a+x /usr/local/sbin/run.sh
RUN sudo sed -i -e 's/\r$//' /usr/local/sbin/run.sh
ENTRYPOINT ["run.sh"]