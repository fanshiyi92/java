### 解决问题
本地开发可能存在一些额外的辅助 API，而测试则调用其他服务；
```
<profiles>
    <profile>
        <id>stg</id>
        <activation>
            <activeByDefault>true</activeByDefault>
        </activation>
    </profile>
    <profile>
        <id>dev</id>
        <activation>
            <activeByDefault>false</activeByDefault>
        </activation>
        <dependencies>
        </dependencies>
    </profile>
</profiles>
```

使用 profiles 修改 pom 文件后,在 idea-maven 中，选择勾选 active 的环境；