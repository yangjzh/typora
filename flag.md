## flag

获取命令行的参数

```go
var period = flag.Duration("period", 1*time.Second, "sleep period")
func main() {
	flag.Parse()
	fmt.Printf("Sleeping for %v...\n", *period)
	fmt.Printf("%T", *period)
	time.Sleep(*period)
	fmt.Println()
}
```

