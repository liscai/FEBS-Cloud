FROM openjdk:8u212-jre
MAINTAINER MrBird 852252810@qq.com

COPY ./target/febs-tx-manager-2.1-RELEASE.jar /febs/febs-tx-manager-2.1-RELEASE.jar
ADD agent/ /agent

ENTRYPOINT ["java", "-javaagent:/agent/skywalking-agent.jar", "-Dskywalking.agent.service_name=febs-tx-manager", "-Dskywalking.collector.backend_service=skywalkingIp:11800", "-jar", "/febs/febs-tx-manager-2.1-RELEASE.jar"]