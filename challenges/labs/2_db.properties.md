
### First lines
```
[root@node02 ~]# head -6 /var/log/cloudera-scm-server/cloudera-scm-server.log
2018-10-19 08:09:30,130 INFO main:com.cloudera.server.cmf.Main: ================================================================================
2018-10-19 08:09:30,146 INFO main:com.cloudera.server.cmf.Main: Starting SCM Server. JVM Args: [-Dlog4j.configuration=file:/etc/cloudera-scm-server/log4j.properties, -Dfile.encoding=UTF-8, -Dcmf.root.logger=INFO,LOGFILE, -Dcmf.log.dir=/var/log/cloudera-scm-server, -Dcmf.log.file=cloudera-scm-server.log, -Dcmf.jetty.threshhold=WARN, -Dcmf.schema.dir=/usr/share/cmf/schema, -Djava.awt.headless=true, -Djava.net.preferIPv4Stack=true, -Dpython.home=/usr/share/cmf/python, -XX:+UseConcMarkSweepGC, -XX:+UseParNewGC, -XX:+HeapDumpOnOutOfMemoryError, -Xmx2G, -XX:MaxPermSize=256m, -XX:+HeapDumpOnOutOfMemoryError, -XX:HeapDumpPath=/tmp, -XX:OnOutOfMemoryError=kill -9 %p], Args: [], Version: 5.14.4 (#3 built by jenkins on 20180707-0445 git: 0971e84bdceb60db9b96533f46451f40ed8cbdf9)
2018-10-19 08:09:30,235 INFO main:org.mortbay.log: Logging to org.slf4j.impl.Log4jLoggerAdapter(org.mortbay.log) via org.mortbay.log.Slf4jLog
2018-10-19 08:09:30,345 INFO main:org.springframework.context.support.ClassPathXmlApplicationContext: Refreshing org.springframework.context.support.ClassPathXmlApplicationContext@30a3107a: startup date [Fri Oct 19 08:09:30 UTC 2018]; root of context hierarchy
2018-10-19 08:09:30,402 INFO main:org.springframework.beans.factory.xml.XmlBeanDefinitionReader: Loading XML bean definitions from class path resource [webapp/WEB-INF/spring/beanRefFactory.xml]
2018-10-19 08:09:30,799 INFO main:org.springframework.beans.factory.support.DefaultListableBeanFactory: Pre-instantiating singletons in org.springframework.beans.factory.support.DefaultListableBeanFactory@776aec5c: defining beans [bootstrapContext,rootContext]; root of factory hierarchy
```

### Jetty line
```
[root@node02 ~]# grep "Started Jetty server" /var/log/cloudera-scm-server/cloudera-scm-server.log
2018-10-19 08:11:16,209 INFO WebServerImpl:com.cloudera.server.cmf.WebServerImpl: Started Jetty server.
```


### db.properties
```
[root@node02 ~]# cat /etc/cloudera-scm-server/db.properties
# Auto-generated by scm_prepare_database.sh on Fri Oct 19 08:08:24 UTC 2018
#
# For information describing how to configure the Cloudera Manager Server
# to connect to databases, see the "Cloudera Manager Installation Guide."
#
com.cloudera.cmf.db.type=mysql
com.cloudera.cmf.db.host=node01.xpandit.com
com.cloudera.cmf.db.name=scm
com.cloudera.cmf.db.user=scm
com.cloudera.cmf.db.setupType=EXTERNAL
com.cloudera.cmf.db.password=scm_password
```
