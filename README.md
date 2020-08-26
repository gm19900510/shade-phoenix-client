# shade-phoenix-client

`phoenix-client`依赖`com.google.guava 16.0`以下版本

`guava 17.0` 为临界版本，做了较大改动，导致版本不兼容

因`phoenix-client`将依赖打包至JAR内，无外部依赖，故与其他组件集成时存在`JAR`冲突问题，顾需解决

解决方案：利用`maven-shade-plugin`，把依赖的包打包进项目的jar，并且`重新命名依赖包的包名`，`将部分依赖排除`，这样编译后形成`shade-phoenix-client-4.14.1-HBase-1.2.jar`

## 安装

- 生成JAR `mvn package`

- 上传至本地私有仓库或将JAR复制到其他项目中使用

## 重要说明

https://www.jianshu.com/p/7a0e20b30401

https://blog.csdn.net/chy2z/article/details/96446936

https://blog.csdn.net/ylb1213/article/details/87095311



