```bash

  docker compose up -d

  # Copy Text File to Node Manager
  docker cp sample.txt nodemanager:/tmp/

  #Copy Program to Node Manager
  docker cp hadoop-mapreduce-examples-2.7.1-sources nodemanager:/tmp/

  hdfs dfs -mkdir -p /user/root/input

  hdfs dfs -put sample.txt /user/root/input
```