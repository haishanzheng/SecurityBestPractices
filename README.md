# 网站开发安全最佳实践

本网站开发安全最佳实践整合自包括哈尔滨工业大学辛毅等多个兄弟高校和互联网的相关文档，涉及服务器、网站开发、美工、移动客户端App等内容。如果需要委托其他软件厂商开发，请把本文档发给对方参考。如果有任何意见或者建议，请发邮件到 vhost # xmu.edu.cn 。也可直接在 https://github.com/haishanzheng/SecurityBestPractices 提交PR。

本最佳实践只聚焦于高校内，较为初级的安全问题。

本最佳实践前方TOC可打印作为checklist要求合作厂商应答。★标较为随意，可自行调整。

TOC使用Atom+Markdown TOC生成。

# 文件结构

- securitybestpractices.md 为最原始文档
- securitybestpractices.html 为Atom+Markdown Preview生成
- securitybestpractices.pdf 为html打印成PDF

HTML和PDF会不定期更新

# TOC

- 厦门大学网站开发安全最佳实践
    - 整体建议
        - □ 是否申请了虚拟机而不是使用自有机房部署
        - □ 是否将新闻性质的网站和信息系统分开
        - □ 是否已通过等保测评
        - □ 是否反向代理友好
        - □ 是否有完善的安全运维维保服务
    - 服务器
        - □ 服务器是否专有用途
        - □ 是否选择了正确的操作系统
        - □ 是否启用了安全更新 ★
        - □ 是否启用了动态磁盘扩展功能
        - □ 是否配置并启用了防火墙 ★
        - □ 是否做了备份 ★
        - □ 是否使用了域名而不是IP部署
        - □ 是否支持IPv6
        - □ 是否支持HTTPS
        - □ 是否支持HTTP2
        - □ 服务器代码和数据等目录是否清晰
        - □ 是否使用了强密码
        - □ 是否使用了监控工具
        - □ 是否部署了软WAF
        - □ 是否不允许Web服务器列出文件
        - □ 是否限制了Web服务器除GET|HEAD|POST以外的方法
        - □ 是否隐藏了Web服务器的Banner信息
        - □ 是否添加了X-Frame-Options不允许网页被嵌入其他网站
        - □ 是否添加了CSP
        - □ 是否有使用漏洞扫描工具扫描服务器和网站
    - 数据库
        - □ 是否应用了独立用户，最小权限原则 ★
        - □ 是否限制了Web数据库管理工具的权限
        - □ 是否没有在源代码版本控制系统里面保存数据库等密码
        - □ 是否正确处理数据库连接串
    - 后台程序
        - □ 是否隐藏了管理员入口
        - □ 是否有使用版本控制系统管理源代码
        - □ 是否有使用框架协助开发
        - □ 是否关闭了调试模式 ★
        - □ 是否有对用户的输入进行检查过滤 ★
        - □ 是否有预防注入漏洞 ★
        - □ 是否有预防跨站脚本攻击 Cross-site scripting (XSS) ★
        - □ 是否有预防跨站域请求伪造 Cross Site Request Forgery (CSRF)
        - □ 是否使用了统一身份认证
        - □ 是否对密码进行了加密保存
        - □ 是否对密码、登录等部分做了防暴力破解检查
        - □ 是否对程序文件所在目录设置只读和不可执行权限设置
        - □ 是否对上次和下载文件进行了全面的保护 ★
        - □ 是否使用UTF8格式保存源代码和展示网页
        - □ 是否考虑了国际化 i18n
        - □ 是否对每个需要登录权限的页面都做了完善的检查 ★
        - □ 是否 OWASP A9:2017 –使用含有已知漏洞的组件
        - □ 是否正确处理了客户端IP获取方法
        - □ 是否有预防 CWE-918: 服务器端请求伪造（SSRF）
    - 网站前端
        - □ 是否有参考了Yahoo!的Best Practices for Speeding Up Your Web Site
    - 页面设计
        - □ 是否已抛弃使用形象首页
        - □ 是否已经不再使用table布局
        - □ 是否采用一些语义化的标签
        - □ 是否有做适合手机和平板浏览的页面
        - □ 是否进行了SEO优化
    - 网站性能
        - □ 是否在上线前对网站性能进行了评估
    - 移动客户端APP
        - □ 是否有通过互联网平台的安全检查 ★
        - □ 是否对代码进行了清理
        - □ 是否对代码进行了混淆
        - □ 是否进行加壳保护
        - □ 是否预防了反编译和二次打包风险
        - □ 是否正确使用了证书对应用进行签名
        - □ 是否防止了Webview File同源策略绕过漏洞
        - □ 是否对传输进行TLS加密 ★
        - □ 是否只请求了必要的系统权限 ★
        - □ 是否将类似accesstoken等保存到客户端
        - □ 是否正确的保护了App的数据库
        - □ 是否对重要信息界面的输入和截屏攻击进行预防
        - □ 是否定期更新打包的框架和第三方SDK
    - 其他
        - □ 是否所有日志都保留6个月并且远程存储 ★


