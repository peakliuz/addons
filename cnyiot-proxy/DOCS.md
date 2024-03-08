# 晨域电表代理服务

## 安装

按照以下步骤将插件安装到系统上:

1. 在您的家庭助理前端导航到**设置**->**加载项**->**附加组件商店**。
2. 找到`cnyiot-proxy`附加组件并单击它。 
3. 点击`安装`按钮。

## 如何使用

1. 在配置部分设置用户名和密码以及调用的秘钥。
2. 保存配置。
3. 启动附加组件。
4. 检查附加组件日志输出以查看结果。

## 如何配置

加载项配置:

```yaml
username: 19xxxx
password: xxxxx
key: xxxx
```
### 参数: `username` (必须)

登录的用户名（电表编号），一般贴在电表的前面，19开头的一串数字。

### 参数: `password` 

登录的密码，默认情况下是123456，不填写默认按照123456。

### 参数: `key` (必须)

调用接口时的验证秘钥。

### 强烈建议
先登录官方提供的平台，测试账号信息，以下方式任选其一即可
- 微信小程序搜索`晨域智控平台`
- 支付宝搜索`晨域智控生活缴费`
- 管理后台[晨域物联科技][cnyiot-boss]

## 如何连接

本项目提供了三个接口

接口名称 | 请求类型 |接口路径
-- |-----| --
获取电表基本信息 | GET | /meterInfo/{key}
获取电表实时信息 | GET | /meterInstant/{key}
获取电表当月用电视图| GET | /meterMonthInfo/{key}

可结合Node-Red或者HomeAssistant命令行调用。
详细的NR配置参考[cnyiot-proxy-nr][cnyiot-proxy-nr]。

## 支持

如有问题，请提[issue][cnyiot-proxy]。

[cnyiot-boss]: https://www.zk.cnyiot.com/cn
[cnyiot-proxy]: https://github.com/peakliuz/cnyiot-proxy
[cnyiot-proxy-nr]:https://github.com/peakliuz/cnyiot-proxy-nr
