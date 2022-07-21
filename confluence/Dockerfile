FROM cptactionhank/atlassian-confluence:7.9.3

USER root

# 将代理破解包加入容器
COPY "atlassian-agent.jar" /opt/atlassian/confluence/
# 将中文字体加入容器
COPY simsun.ttc /usr/share/fonts/chinese/

# 设置启动加载代理包
RUN echo 'export CATALINA_OPTS="-javaagent:/opt/atlassian/confluence/atlassian-agent.jar ${CATALINA_OPTS}"' >> /opt/atlassian/confluence/bin/setenv.sh
# 设置启动加载所需字体
RUN echo 'export CATALINA_OPTS="-Dconfluence.document.conversion.fontpath=/usr/share/fonts/chinese/ ${CATALINA_OPTS}"' >> /opt/atlassian/confluence/bin/setenv.sh