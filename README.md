# sentinel
1.在springboot代码中引入sentinel依赖，如下所示：

<dependency>
    <groupId>com.alibaba.cloud</groupId>
    <artifactId>spring-cloud-starter-alibaba-sentinel</artifactId>
    <version>2.2.1.RELEASE</version>
</dependency>

2.打包镜像，跟普通Dockerfile一样，不需要加其他额外的变量参数

4.部署sentinel，详见sentinel.yaml文件

6.部署微服务应用，详见nginx.yaml文件

8.说明

nginx.yaml文件是第二步打包后的微服务，需要注意的是
需要添加sentinel的环境变量参数，这是sentinel的web端地址；
          - name: "spring.cloud.sentinel.transport.dashboard"
            value: "192.168.0.170:30101"
