
### JINGLI 鲸哩充电桩云平台（含硬件充电桩）（v2.3.2）

> 我的车，到底该选什么功率充电桩： [点我访问](https://blog.csdn.net/Roinli/article/details/127148030?spm=1001.2014.3001.5501)

> 体验地址，star star ： [点我访问](http://charge.nxptdn.com)


#### 日志记录

> 每天进步一点点，希望每天能更新一些进度。

> [系统更新日志](http://www.nxptdn.com/article/39) 

 
#### 一，平台简介
JINGLI 鲸哩充电桩云平台（含硬件充电桩）（v2.3.2）包括了前端uniapp（公众号、H5、小程序）、采集端、运营端、代理商端、充电桩硬件（电动自行车、电动汽车），平台目前服务企业100+，采用SpringBoot、SpringCloud、MySQL、Netty、MQTT、支付宝支付、微信支付、微信退款、支付宝退款等技术栈
1. JINGLI 鲸哩充电桩云平台（含硬件充电桩）（v2.3.2），从（采集端-用户端-商户端-平台端）全业务场景，开源版本免费提供。
2. 初衷，发现很多开源的产品缺东西，比如缺公众号，比如缺硬件对接的协议，我们希开源一套只要懂java的开发人员就能进行部署使用。
3. 初心：做了很多产品项目都商业落地了但是仅仅服务商业本身无法释放产品的价值，不在重复造轮子，让更多的企业和个人能够减少投入，先star欢迎讨论交流加群，微信18601938676
#### 二，整体设计图（流程）
  <img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.1/img/1.jpg"/>

#### 三，平台组成


----

```
1. 采集端：使用Netty、mqtt采集充电桩信息
2. 用户端：负责用户的充电全套流程；使用小程序/H5/uniapp
3. 后台端：负责管理整体平台数据以及代理商数据
4. 商户端：某个区域的代理商数据管理
```
#### 四，软件架构
```
1. 采集端：Netty、MQTT负责采集设备数据
2. 用户端：①vue / uniapp（前端）      ②微信公众号API、SpringBoot、SpringCloud、Mybatis(后端)
3. 商户端：①vue / uniapp（前端）      ②微信公众号API、SpringBoot、SpringCloud、Mybatis(后端)
4. 运行端：①vue-admin-template(前端)  ②SpringBoot、SpringCloud、Mybatis        (后端)
5. 数据库：MySQL
```
#### 五，代码结构

```
└─ jingli                                                JINGLI 鲸哩充电桩云平台（含硬件充电桩）（v2.3.2）
    ├─ open-smart-charge-operator-back                   平台端：接口
    ├─ open-smart-charge-operator-front                  平台端：前端
    ├─ open-smart-charge-wechat-font                     用户端：前端
    └─ open-smart-charge-wechat-service                  ①采集端：Netty、Mqtt  ②用户后端接口 ③用户端微信API 
```


#### 六，产品功能

##### 整体功能说明
第一部分平台用户核心流程说明：
    用户使用微信公众号扫描设备，选择端口，
    选择充电时长微信支付费用或选择设备充电完成自动扣款两种模式，
    插上充电口充电。
第二部分代理商saas模式说明（可选）：
    平台开发代理商模式即代理商自行购买设备，代理商自行设置收费模式、自行计费、以及设备的管理等功能。

##### 特别说明
目前产品已经落地实施，为了满足实际的应用场景，我们根据使用需求进行了大量的细节修改比如运营端进行设备退费，细节做了很多，满足实际场景需要。

#### 七，团队计划
```
- 用心做产品，不以赚钱为目的。
- 搭建基础性行者物联网快速开发平台。
- 软件架构升级SpringCloud/产品细节优化
- 推广促进更多厂家和硬件开发者接入开源充电桩Saas系统（v2.3.2）
- 以前做过：智能充电桩云平台，AI计算中心，智慧农业，智慧工业，高效节水，水肥一体化，污水处理，计量计费，水质检测，智慧大棚，农业项目
```
#### 八，部分截图
##### 平台端
<table>
    <tr>
        <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.2/2022.11.10%20%E5%85%85%E7%94%B5%E6%A1%A9PC/Cdz-0701-%E7%99%BB%E5%BD%95.jpg"/></td>
    </tr>
    <tr>
            <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.2/2022.11.10%20%E5%85%85%E7%94%B5%E6%A1%A9PC/Cdz-%E7%BB%9F%E8%AE%A1-%E7%94%A8%E6%88%B7.jpg"/></td>
        </tr>
    <tr>
        <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.2/2022.11.10%20%E5%85%85%E7%94%B5%E6%A1%A9PC/Cdz-%E7%BB%9F%E8%AE%A1-%E9%94%80%E5%94%AE.jpg"/></td>
    </tr>
</table>

##### 用户端
<table>
    <tr>
        <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.2/2022.11.11%202036/1-%E4%B8%BB%E9%A1%B5.jpg"/></td>
        <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.2/2022.11.11%202036/2-%E5%85%85%E7%94%B5%E6%A1%A9%E8%AF%A6%E7%BB%86%E9%A1%B5.jpg"/></td>
    </tr>
    <tr>
        <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.2/2022.11.11%202036/4-%E6%88%91%E7%9A%84.jpg"/></td>
        <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.2/2022.11.11%202036/5-%E4%BD%99%E9%A2%9D%E5%85%85%E5%80%BC.jpg"/></td>
    </tr>
</table>

##### 商户端
<table>
    <tr>
        <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.2/2022.11.11%202036/%E4%BB%A3%E7%90%86%E5%95%86-1-%E7%99%BB%E5%BD%95%E9%A1%B5.jpg"/></td>
        <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.2/2022.11.11%202036/%E4%BB%A3%E7%90%86%E5%95%86-3-%E8%AE%BE%E5%A4%87%E8%AF%A6%E6%83%85.jpg"/></td>
    </tr>
</table>

#### 九，如何部署
```
请参考每个工程都有READEME.md文档（详细部署文档）
```
#### 十，JINGLI 鲸哩充电桩云平台（含硬件充电桩）（v2.3.2）

#### 十一、核心开发团队
产品：周立

技术：文哥、小兵、亮亮、喜峰、周强、单单、于强、明哥、小杨

UI：ZLY、ZMD

测试：冬天、蜗牛、小强

硬件：亮、峰哥

#### 十二，更新信息：

http://www.nxptdn.com/
