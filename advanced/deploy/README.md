# 本地部署

除了使用在线的形式生成代码，您还可以通过将faster-builder启动包下载到本地运行，目前我们提供了编译好的jar包，您可以在github中选择合适的版本下载。

[下载地址](https://github.com/faster-framework/faster-framework-builder/releases)

每次发行版中都明确指明了该jar包可以生成的faster套件版本，下载后在本地通过以下命令运行：

```
java -jar faster-framework-builder-{version}.RELEASE.jar
```

成功运行后，通过访问以下地址进行生成代码：

```
http://localhost:8080
```