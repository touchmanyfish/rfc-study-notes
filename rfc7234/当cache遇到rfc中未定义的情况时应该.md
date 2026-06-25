# 当cache遇到rfc中未定义的情况时应该

## 感觉

当在实现cache时遇到了rfc没有明确定义的情况，cache在自行处理的同时需要遵守的通用准则有哪些？

gemini说Okhttp在遇到rfc未定义的情况时，遵循"保守且透明"原则，哦f**，不知道该怎么写了。


**目前感觉**：
* 收到一个request遇到不能处理的情况就forward到server
* 收到一个response遇到不能处理的情况就forward到client
