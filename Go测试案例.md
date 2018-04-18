## GO测试案例原理

导入测试包

`import "testing"`

测试文件以*_test.go结尾

测试函数名字以Test开头

```
func TestSin(t *testing.T) { /* ... */ }
```

使用t.Fatal或t.Fatalf停止当前测试函数。它们必须在和测试函数同一个goroutine内调用。

使用t.Errorf打印失败信息