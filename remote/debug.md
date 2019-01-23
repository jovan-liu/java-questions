# 配置远程调试debug模式：
## 在tomcat下配置debug模式

在${tomcat_home}/bin/catalina.sh中配置以下信息

`SET CATALINA_OPTS=-server -Xdebug -Xnoagent -Djava.compiler=NONE -Xrunjdwp:transport=dt_socket,server=y,suspend=n,address=8000`

## 使用java -jar的方式配置debug模式

1. 在cmd中使用以下参数进行配置

`java -jar -Xdebug -Xrunjdwp:transport=dt_socket,server=y,suspend=n,address=8000 springboot-app-1.0-SNAPSHOT.jar`

2. 在bat文件中进行配置

```
set "JAVA_OPT=%JAVA_OPT% -Xdebug -Xrunjdwp:transport=dt_socket,server=y,suspend=n,address=8000"
```
