v1版本
安全部署注意事项
1. 部署位置建议
● 推荐将本页面部署在独立子域名（如 video.企业.com），不要与主站共享同源，以降低Cookie可能对主站造成的危害。
● 如果必须放在主站子目录下，请确保主站的Cookie设置了 SameSite=Lax 或 Strict，且作用域不包含子路径。
2. 自定义扩展
● 若需自定义扩展，请防止XSS注入，请遵循“永远不要信任用户输入”原则，必须执行的代码安全检查。
3. 如果使用 iframe 嵌入
● 请在父页面设置 <iframe sandbox="allow-same-origin allow-scripts allow-popups allow-forms" src="...">，限制不必要的权限