

## 添加方式
1. 先在cloudflare上面拥有一个域名，请自行搜索教程
2. 进入worker也能，点击创建
<img src="../img/cloudflare1.png" width="800"/>
3. 点击“从 Hello World! 开始”旁边的按钮
<img src="../img/cloudflare2.png" width="800"/>
4. 取个名字，点击部署
5. 点击代码
<img src="../img/cloudflare3.png" width="800"/>
6. copy代码
- [代码](./反代程序/proxy.js)
7. 点击部署
![img_2.png](img_2.png)
8. 进入设置，添加一个自定义域
![img_3.png](img_3.png)
9. 填入的域名放到配置ProxyUrl
![img_4.png](img_4.png)
![img_5.png](img_5.png)
注意： 这个域名为参数: ProxyUrl 的值，记得加入https://域名