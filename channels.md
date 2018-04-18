# Channels

- channels是一个通道机制，可以让一个goroutine 通过它给另一个goroutine发送消息
- 接收者收到数据发生在唤醒发送者goroutine之前
- 使用内置的close函数可以关闭一个channel，随后对基于该channel的任何发送操作都将导致panic异常

```go
ch := make(chan int) #无缓冲
ch := make(chan int,2) #有缓冲通道
ch <- x  //发送
x = <-ch //接收
<-ch     //接收丢弃

```



