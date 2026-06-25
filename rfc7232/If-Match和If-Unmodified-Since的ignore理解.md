# If-Match和If-Unmodified-Since的ignore理解

```text
 The If-Match header field can be ignored by caches and intermediaries
   because it is not applicable to a stored response.
   
 The If-Unmodified-Since header field can be ignored by caches and
   intermediaries because it is not applicable to a stored response.  
```
关于“ignored”，我最开始理解的是，cache无视If-Match/If-Unmodified-Since，接着处理剩下的If-x。但是这么理解用户的意图不会得到执行，例如If-Match表示用户期望去origin server
进行验证，但是cache却私自进行处理了。

gemini说，“ignored”表示，cache处理不了就不要私自处理，默认往下一跳转发。感觉这样理解要合理一点，用户意图也得以保留。（**RFC_GUSS**）

