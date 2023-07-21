FROM hadoop-hive-spark-base

COPY run.sh /usr/local/sbin/
RUN sudo chmod a+x /usr/local/sbin/run.sh
RUN sudo sed -i -e 's/\r$//' /usr/local/sbin/run.sh
ENTRYPOINT ["run.sh"]