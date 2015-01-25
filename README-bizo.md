
export MAVEN_OPTS="-Xmx2g -XX:MaxPermSize=512m"

./make-distribution.sh --name "hadoop2.4" --tgz -Phadoop-2.4 -Pscala-2.11

version=1.1.1-rc2
s3cp spark-$version-bin-hadoop2.4.tgz s3://com-bizo-repository-v2/bizo.com/spark-prebuilt_2.11/default/tgzs/spark-$version-hadoop-2.4.0-prebuilt.tgz


