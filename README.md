# 实验二：Android 网络访问

## 一、实验目标

完成 Android 应用的网络访问实验，验证 HTTPS 与 HTTP 网络请求的区别，并学习 Android 网络安全配置。

## 二、运行方式

使用 Android Studio 打开项目 FirstKotlinApp。

连接 Android 模拟器或 Android 真机后运行项目。

进入应用后，可以点击“HTTPS 请求”和“HTTP 请求”按钮进行网络访问测试。

## 三、接口地址

HTTPS：
https://httpbin.org/get?room=A203

HTTP：
http://httpbin.org/get?room=A203

实验中将 room 参数修改为 A204 进行参数验证。

## 四、网络安全配置

默认禁止 HTTP 明文通信，仅允许指定的 httpbin.org 使用 HTTP 明文通信。

## 五、说明

HTTP 仅用于本次实验的教学对比，实际服务应优先使用 HTTPS。