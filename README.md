# 电脑（Widows）如何通过V2rayN双层代理方式使用Sock5 IP

对于做跨境业务的朋友来说，电脑上如何通过v2rayN代理使用Socks5 ip，操作如下：

## 首先打开你的v2rayN

![首先打开你的v2rayN](https://tarticle.oss-cn-shenzhen.aliyuncs.com/article/medium_1_f73bd37282.png)

## 一、添加 S5 前置节点

点击顶部「服务器」→「添加 [Socks] 服务器」，填写 S5 信息（地址、端口、用户名 / 密码），别名设为 S5-Pre（方便识别），点击「确定」。

![添加 S5 前置节点](https://tarticle.oss-cn-shenzhen.aliyuncs.com/article/medium_2_932b24f886.png)

## 二、  新建链式分组

点击顶部「订阅分组」→「订阅分组设置」→「添加」，填写分组名称（如「S5 链式分组」），关键设置：前置代理别名选择1标签的别名（如此图叫公司专线），落地代理别名选择刚添加的 S5-Pre，点击「确定」。

![新建链式分组](https://tarticle.oss-cn-shenzhen.aliyuncs.com/article/medium_3_1_8c403c1003.jpg)

![s5链式分组](https://tarticle.oss-cn-shenzhen.aliyuncs.com/article/medium_4_5ede50d991.png)

之后关闭上面窗口。

## 三、复制目标节点到链式分组

选中添加的目标节点如标签2窗口，利用快捷键复制一下Ctrl+C，Ctrl+V粘贴到「S5 链式分组」

![选中添加的目标节点如标签2窗口，利用快捷键复制一下Ctrl+C](https://tarticle.oss-cn-shenzhen.aliyuncs.com/article/medium_5_1118216f45.png)

![Ctrl+V粘贴到「S5 链式分组」](https://tarticle.oss-cn-shenzhen.aliyuncs.com/article/medium_6_96d582ab8b.png)

## 四、启用链式代理

选中分组内的目标节点，右键「设为活动服务器」，开启「Tun 模式」（若需全局代理），右键托盘图标→「自动配置系统代理」。

![启用链式代理」](https://tarticle.oss-cn-shenzhen.aliyuncs.com/article/medium_7_5ab397d8d0.png)

## 五、验证是否生效

开启代理后，访问 IP 查询网站（如https://www.ipaddress.com/）， 显示的 IP 应为 S5 服务器的 IP，说明链式代理生效。或者测试目标网站 / 服务，确认网络访问正常。
