# protocol-buffers
## 官网git：https://github.com/protocolbuffers/protobuf
## JAVA：https://github.com/protocolbuffers/protobuf/tree/master/java
## 1. 使用前准备
要在Java中使用protobuf，请首先获取协议编译器，然后使用它为您的.proto文件生成Java代码：
```
$ protoc --java_out=${OUTPUT_DIR} path/to/your/proto/file
```
编译器下载地址：  
https://github.com/protocolbuffers/protobuf/releases  
这里我们下载window的64位版本，在本地可以直接使用：  
https://github.com/protocolbuffers/protobuf/releases/download/v3.15.6/protoc-3.15.6-win64.zip  
解压后再bin目录下的protoc.exe就是我们所需编译器文件  
编译：
```
protoc.exe --java_out=${OUTPUT_DIR} path/to/your/proto/file
```
## 2. 编写JAVA
### 2.1 引用依赖
确保运行时的版本号与协议的版本号匹配（或比其新）
```
<dependency>
  <groupId>com.google.protobuf</groupId>
  <artifactId>protobuf-java</artifactId>
  <version>3.15.3</version>
</dependency>
``` 
如果要使用protobuf JsonFormat之类的功能，请在protobuf-java-util包上添加一个依赖项：  
```
<dependency>
  <groupId>com.google.protobuf</groupId>
  <artifactId>protobuf-java-util</artifactId>
  <version>3.15.3</version>
</dependency>
```

