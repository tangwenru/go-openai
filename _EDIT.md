# 修改记录

# 一
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

# 二
`github.com/sashabaranov/go-openai` 改为 `github.com/tangwenru/go-openai`