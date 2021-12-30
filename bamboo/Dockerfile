FROM cptactionhank/atlassian-bamboo:latest

USER root

# 将代理破解包加入容器
COPY "atlassian-agent.jar" /opt/atlassian/bamboo/

# 设置启动加载代理包
RUN echo 'export CATALINA_OPTS="-javaagent:/opt/atlassian/bamboo/atlassian-agent.jar ${CATALINA_OPTS}"' >> /opt/atlassian/bamboo/bin/setenv.sh