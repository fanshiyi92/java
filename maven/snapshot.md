### 问题及原因
测试环境，因为运维组部署的 jenkins 配置，本地 maven repository 不存在 jar,才会从远程 maven 拉取；
而当使用 SNAPSHOT 时，测试服务器 repository 不会去更新最新 jar;
### 解决办法
```
<snapshots>
    <enabled>true</enabled>
    <updatePolicy>always</updatePolicy>
    <checksumPolicy>fail</checksumPolicy>
</snapshots>
```
配置修改 pom.xml，如果是快照结尾的依赖都会重新拉取；