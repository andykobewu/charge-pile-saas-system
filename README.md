
### 鲸哩开源充电桩Saas系统（v2.3.1）

> 我的车，到底该选什么功率充电桩： [点我访问](https://blog.csdn.net/Roinli/article/details/127148030?spm=1001.2014.3001.5501)

> 体验地址，star star ： [点我访问](http://charge.nxptdn.com)

#### 日志记录

> [系统更新日志](http://www.nxptdn.com/article/39) 


 
#### 一，平台简介
鲸哩开源充电桩Saas系统（v2.3.1）包括了前端（公众号、H5、小程序、uniapp）、采集端、运营端、代理商端、充电桩硬件（电动自行车、电动汽车），平台目前服务企业100+，采用SpringBoot、SpringCloud、MySQL、Netty、MQTT、支付宝支付、微信支付、微信退款、支付宝退款等技术栈
1. 鲸哩开源充电桩Saas系统（v2.3.1），从（采集端-用户端-代理商-平台端）全业务场景，开源版本免费提供。
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
4. 代理商：某个区域的代理商数据管理
```
#### 四，软件架构
```
1. 采集端：Netty、MQTT负责采集设备数据
2. 用户端：①vue / uniapp（前端）      ②微信公众号API、SpringBoot、SpringCloud、Mybatis(后端)
3. 代理端：①vue / uniapp（前端）      ②微信公众号API、SpringBoot、SpringCloud、Mybatis(后端)
4. 运行端：①vue-admin-template(前端)  ②SpringBoot、SpringCloud、Mybatis        (后端)
5. 数据库：MySQL
```
#### 五，代码结构

```
└─ jingli                                                鲸哩开源充电桩Saas系统（v2.3.1）
    ├─ open-smart-charge-operator-back                   运营端：接口
    ├─ open-smart-charge-operator-front                  运营端：前端
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
- 推广促进更多厂家和硬件开发者接入鲸哩开源充电桩Saas系统（v2.3.1）
- 以前做过：智能充电桩云平台，AI计算中心，智慧农业，智慧工业，高效节水，水肥一体化，污水处理，计量计费，水质检测，智慧大棚，农业项目
```
#### 八，部分截图
##### 后台
<table>
    <tr>
        <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.1/img/2.png"/></td>
    </tr>
    <tr>
            <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.1/img/3.png"/></td>
        </tr>
    <tr>
        <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.1/img/4.png"/></td>
    </tr>
</table>

##### 用户端
<table>
    <tr>
        <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.1/img/8sj.png"/></td>
        <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.1/img/9.png"/></td>
    </tr>
    <tr>
        <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.1/img/10.png"/></td>
        <td><img src="https://wenhui-1251454246.cos.ap-nanjing.myqcloud.com/cdz/v2.3.1/img/11.png"/></td>
    </tr>
</table>

##### 代理商


#### 九，如何部署
```
请参考每个工程都有READEME.md文档（详细部署文档）
```
#### 十，鲸哩开源充电桩Saas系统（v2.3.1）由宁夏普天动能信息技术有限公司投资建设。
#### 十一，代码贡献者鸣谢
京东(JD) java工程师 文哥、java工程师 波哥、硬件工程师 亮哥、前端工程师 小兵、UI设计 周同学、产品 小魏，希望更多的跟个人和企业减少重复造轮子
减少投入。

#### 十二，官方网站：

http://www.nxptdn.com/
