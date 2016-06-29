##Description
This image is built from chronos 2.4.0 and mesos 0.26.0
##docker build
```
docker build -f Dockerfile -t supernova106/chronos:2.4.0-0.26.0 .
```
##docker run
```
docker run -d -e CHRONOS_HTTP_PORT=4400 \
	-e CHRONOS_MASTER='zk://' \
	-e CHRONOS_ZK_HOSTS='' \
	--name chronos \
	--net=host \
	supernova106/chronos:2.4.0-0.26.0
```
## Marathon deployment
- ignore CHRONOS_HTTP_PORT, the port will be dynamically assigned via ENV variable $PORT0 in HOST network mode


