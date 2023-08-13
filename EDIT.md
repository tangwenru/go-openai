# 修改记录
文件 `config.go`

```go
// 2023-08-10
func NewClient(authToken string, baseURL string) *Client {
    config := DefaultConfig(authToken)
+    if baseURL != ""{
+       config.BaseURL = baseURL
+    }
    return NewClientWithConfig(config)
}
```