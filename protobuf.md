# Protobuf

​	ProtoBuf 是一种数据表达方式，根据 G 家自己的描述，应该叫做**数据交换格式**，注意这里使用的是 **交换** 字眼，也就是说着重于在数据的传输上，有别于 TOML 和 XML 较常用于配置（当然 WebService 一套也是用于数据交换）。	

proto 的语法有点类似于定义一个类或者说结构体更合适一些，因为它没有方法，只有属性，一个简单的示例为：

```protobuf
sysntax = "proto3";
message SearchRequest{
    string query = 1;
    int32 page_number =2;
    int32 result_per_page = 3;
}
```

1. 第1行肯定是需要的，表名你用的哪个版本，这里指明我得语法是proto3版本
2. 第3行这里就可以理解成定义了一个结构体，名字叫做：SearchRequest
3. 第4-6行就是定义了结构体的属性了，类型+名字

使用命令生成代码

protoc --go_out=plugins=grpc:. *.proto

