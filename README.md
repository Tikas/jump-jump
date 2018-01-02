# jump-jump

**微信小游戏跳一跳作弊**

### 如何抓包拿到session_id?
  
1. 下载最新`charles`。
2. 启动`charles`。
3. 在`Proxy Settings`配置中勾上`Enable transparent HTTP proxying`。
4. 在`SSL Proxying Settings`配置中勾上`Enable SSL Proxying`, 并添加一个空白配置(`*`)。
4. 手机配置代理：设置 > 无线局域网 > 配置代理 > 手动 > IP:电脑ip, 端口:8888。
5. 导入https证书：浏览器访问[http://chls.pro/ssl](http://chls.pro/ssl)下载安装证书。
6. 启动跳一跳小程序，不用点开始。
7. 去`charles`里查看抓到的请求,例如`https://mp.weixin.qq.com/wxagame/wxagame_init`路径的请求，请求体里就包含`session_id`。

*使用fiddler抓包也可以。*

### 使用步骤

1. 拿到`session_id`并手动替换`index.js`文件中`session_id`变量的值。
2. 安装依赖。
    ```
    npm i
    ```
3. 运行。
    ```
    npm start
    ```

### 参考
- [https://gist.github.com/feix/6dd1f62a54c5efa10f1e1c24f8efc417](https://gist.github.com/feix/6dd1f62a54c5efa10f1e1c24f8efc417)