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

## 实验三：Android 工程结构与校园巡检页面

### 运行方法
1. 使用 Android Studio 打开 FirstKotlinApp 工程。
2. 等待 Gradle 同步完成。
3. 连接 Android 模拟器或真机。
4. 运行 app 模块。
5. 在校园巡检页面点击“请求 A203”或“请求 A204”，查看 HTTPS 请求结果。

### 源码文件职责
- `MainActivity.kt`：应用入口，设置 Compose 页面，管理请求状态并更新响应结果。
- `InspectionScreen.kt`：显示巡检员、实验室、设备数量和请求按钮，计算未检查数量。
- `InspectionNetwork.kt`：使用 OkHttp 发送 HTTPS 请求，读取 HTTP 响应并处理异常。

### 网络依赖
- OkHttp：`com.squareup.okhttp3:okhttp:4.12.0`

### 测试接口
- A203：`https://httpbin.org/get?room=A203`
- A204：`https://httpbin.org/get?room=A204`

本实验使用公共回显接口验证请求参数，不涉及真实巡检任务获取或巡检记录保存。
