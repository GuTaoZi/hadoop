## Apache Hadoop 3.3.6 Source Code

This is the source code of Apache Hadoop, from [branch-3.3.6](https://github.com/apache/hadoop/tree/branch-3.3.6).

Slight modifications applied to build jar files from source.

### Guide for building from source

1. Install Docker
2. Execute `./start-build-env.sh`
3. Enter the container by `docker exec -it hadoop-build bash`
4. Inside the container, use Maven to compile and build jar files into `**/target`

**Example**

```sh
./start-build-env.sh

# modify the source code of MRBench.java
# build MRBench
cd hadoop-mapreduce-project/hadoop-mapreduce-client/hadoop-mapreduce-client-jobclient
mvn package -DskipTests -Dmaven.javadoc.skip=true
```