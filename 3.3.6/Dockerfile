FROM apache/hadoop:3.3.6

ENV HADOOP_HOME		/opt/hadoop
ENV HADOOP_CONF_DIR	$HADOOP_HOME/etc/hadoop

# Allow running daemons as root inside the container
ENV HDFS_NAMENODE_USER		root
ENV HDFS_DATANODE_USER		root
ENV YARN_RESOURCEMANAGER_USER	root
ENV YARN_NODEMANAGER_USER	root

# Overwrite default Hadoop configuration with our config files
COPY conf $HADOOP_CONF_DIR/

# Helper script (optional)
ADD start-yarn.sh /usr/local/bin/start-yarn.sh

# Expose commonly used ports
EXPOSE 9000 9870 9866 9867 9864 9868 8088
