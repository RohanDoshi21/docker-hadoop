```bash

  docker compose up -d

  # Copy Text File to Node Manager
  docker cp sample.txt namenode:/tmp/

  #Copy Program to Node Manager
  docker cp hadoop-mapreduce-examples-2.7.1-sources.jar namenode:/tmp/

  docker exec -it namenode /bin/bash

  cd tmp

  hdfs dfs -mkdir -p /user/root/input

  hdfs dfs -put sample.txt /user/root/input

  hadoop jar hadoop-mapreduce-examples-2.7.1-sources.jar org.apache.hadoop.examples.WordCount input /output

  hdfs dfs -ls /output

  hdfs dfs -get /output /tmp

  exit

  docker cp namenode:/tmp/output .

  # View your file in output folder/part-r-00000
```