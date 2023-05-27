# OpenDRG的目标是成为国家医保局CHS-DRG的开源实现，就像OpenJDK是Java SE的开源实现一样

## 业务背景

&emsp;&emsp;疾病诊断相关组（Diagnosis Related Groups，DRG）是用于衡量医疗服务质量效率以及进行医保支付的重要工具。国家医保局已经出台文件，要求从2022到2024年，三年内全面完成DRG/DIP付费方式改革，很多省市医保局已经采用DRG方式与医院进行结算。医院为了应对DRG支付改革，需要掌握DRG分组规则。但是各地DRG分组规则不统一，经常变化，医院很难通过自行研究去掌握。如果花高价去采购商业DRG软件，一方面软件厂商在各地规则的研究方面，水平参差不齐，很多时候不能及时满足需求；另一方面，大部分厂商的软件是封闭式的，医院不能自由的调用底层分组接口或者进行二次开发，尤其很难满足大批量数据分析方面的需求。

&emsp;&emsp;我们一批志同道合的的小伙伴，花费大量时间精力，学习DRG理论、研究国家DRG政策、跟踪各省市的DRG改革进程，并且研发了DRG分组器软件，在一些地区成功实践。为了帮助更多的医院解决DRG难题，助力国家DRG改革，我们在“开放源代码软件”运动的启发下，决定按照“开放、透明、协作、交付”的原则，向全国的医院免费提供OpenDRG分组器源代码，并欢迎所有的信息化厂商进行集成。

## OpenDRG分组器产品优势
* 严格按照医保局规则进行分组，其正确性经过多个地区、多家医院的实际验证
* 以插件方式嵌入医院业务系统运行，不需要部署服务器，不增加医院服务器负担
* 采用Java、C#、python、js等多种语言实现，方便医院HIS、EMR、病案等不同技术架构的系统来集成
* 性能非常高，5000份病案的分组，最多只要1秒钟，即满足日常业务处理，也能应用到大数据分析场景
* 采用开源方式运作，很多业内有志之士提供支持，不管是分组规则还是软件功能，都更新非常快
* 如果以上优势都不能吸引你，再看看这最后一项：**它永久免费提供，不谋求任何商业利益！！！**

## 各地方分组方案支持情况
|省份|城市|DRG基础版本|更新年度|DRG组数|本地化<br>细分组|测试链接|
|-|-|-|-|-|-|-|
|北京|-|CHS-DRG 1.1|2022年|696组|是|[beijing_2022](https://opendrg.github.io?type=beijing_2022)|
|浙江|-|ZJ-DRG 1.1|2022年|1006组|是|[zhejiang_2022](https://opendrg.github.io?type=zhejiang_2022)|
|广西|-|CHS-DRG 1.1|2022年|984组|是|[guangxi_2022](https://opendrg.github.io?type=guangxi_2022)|
|云南|-|CHS-DRG 1.1|2022年|677组|是|[yunnan_2022](https://opendrg.github.io?type=yunnan_2022)|
|江苏|盐城|CHS-DRG 1.1|2023年|628组|否|[yancheng_2023](https://opendrg.github.io?type=yancheng_2023)|
|江苏|苏州|CHS-DRG 1.1|2023年|667组|是|[suzhou_2023](https://opendrg.github.io?type=suzhou_2023)|
|江苏|泰州|CHS-DRG 1.1|2022年|758组|是|[taizhou_2022](https://opendrg.github.io?type=taizhou_2022)|
|江苏|无锡|CHS-DRG 1.1|2022年|599组|是|[wuxi_2022](https://opendrg.github.io?type=wuxi_2022)|
|江苏|常州|CHS-DRG 1.1|2022年|740组|是|[changzhou_2022](https://opendrg.github.io?type=changzhou_2022)|
|山东|济南|CHS-DRG 1.1|2022年|887组|否|[jinan_2023](https://opendrg.github.io?type=jinan_2023)|
|山东|临沂|CHS-DRG 1.1|2022年|628组|否|[linyi_2022](https://opendrg.github.io?type=linyi_2022)|
|山东|青岛|CHS-DRG 1.1|2023年|682组|是|[qingdao_2023](https://opendrg.github.io?type=qingdao_2023)|
|山东|聊城|CHS-DRG 1.1|2022年|683组|是|[liaocheng_2022](https://opendrg.github.io?type=liaocheng_2022)|
|山东|烟台|CHS-DRG 1.1|2023年|647组|是|[yantai_2023](https://opendrg.github.io?type=yantai_2023)|
|福建|福州|CHS-DRG 1.1|2022年|563组|是|[fuzhou_2022](https://opendrg.github.io?type=fuzhou_2022)|
|福建|南平|CHS-DRG 1.1|2023年|795组|是|[nanping_2023](https://opendrg.github.io?type=nanping_2023)|
|陕西|西安|CHS-DRG 1.0|2020年|618组|否|[xian_2020](https://opendrg.github.io?type=xian_2020)|
|陕西|铜川|CHS-DRG 1.1|2022年|628组|否|[tongchuan_2022](https://opendrg.github.io?type=tongchuan_2022)|
|贵州|六盘水|CHS-DRG 1.1|2022年|628组|否|[chs_drg_11](https://opendrg.github.io?type=chs_drg_11)|
|贵州|铜仁|CHS-DRG 1.1|2022年|628组|否|[chs_drg_11](https://opendrg.github.io?type=chs_drg_11)|
|四川|成都|CHS-DRG 1.0|2022年|618组|否|[chengdu_2022](https://opendrg.github.io?type=chengdu_2022)|
|湖北|武汉|CHS-DRG 1.0|2022年|660组|是|[wuhan_2022](https://opendrg.github.io?type=wuhan_2022)|
|湖南|长沙市<br>株洲市<br>湘潭市<br>衡阳市|CHS-DRG 1.1|2023年|737组|是|[changsha_2023](https://opendrg.github.io?type=changsha_2023)|
|山西|临汾|CHS-DRG 1.1|2022年|645组|是|[linfen_2022](https://opendrg.github.io?type=linfen_2022)|
|甘肃|兰州|CHS-DRG 1.1|2023年|794组|是|[lanzhou_2023](https://opendrg.github.io?type=lanzhou_2023)|
|宁夏|银川|CHS-DRG 1.1|2023年|639组|是|[yinchuan_2023](https://opendrg.github.io?type=yinchuan_2023)|
|新疆|乌鲁木齐市|CHS-DRG 1.1|2022年|718组|是|[wlmq_2022](https://opendrg.github.io?type=wlmq_2022)|
|新疆|生产建设<br>兵团|CHS-DRG 1.1|2022年|635组|是|[xjbt_2022](https://opendrg.github.io?type=xjbt_2022)|
|黑龙江|哈尔滨|CHS-DRG 1.1|2022年|668组|是|[haerbin_2022](https://opendrg.github.io?type=haerbin_2022)|
|河南|安阳|CHS-DRG 1.1|2021年|802组|是|[anyang_2021](https://opendrg.github.io?type=anyang_2021)|
|广东|佛山|CHS-DRG 1.1|2022年|848组|是|[foshan_2022](https://opendrg.github.io?type=foshan_2022)|
|安徽|合肥|CHS-DRG 1.1|2023年|851组|是|[hefei_2023](https://opendrg.github.io?type=hefei_2023)|

&emsp;&emsp;江苏徐州、四川自贡、河南开封、辽宁沈阳等地区版本的分组器正在开发，将逐步发布，敬请关注！

## 子项目介绍
### DRG_Rules
&emsp;&emsp;国家医保局CHS-DRG、浙江ZJ-DRG，以及北京等省医保局发布的分组方案文件，经过结构化处理后形成的知识库
### DRG_Datas
&emsp;&emsp;DRG分组相关的各类数据集，包括不同版本的ICD编码、各地医保局的分组权重及支付标准、各类医院病案数据文件等
### DRG_Java/DRG_Csharp/DRG_Python/DRG_JavaScript
&emsp;&emsp;Java、Csharp、Python、JavaScript四种不同语言开发的DRG分组器源代码，功能实现完全一致，可直接使用或集成到医院内部各种业务系统
### opendrg.github.io
&emsp;&emsp;分组器演示平台，一个简单的网页，集成了JavaScript版本的分组器，可以按不同省市的分组方案对病案进行分组，并显示分组结果、支付信息及统计指标等

## DRG分组器演示平台 
* 网址：[opendrg.github.io](https://opendrg.github.io/)

* 网页加载会有点慢，因为DRG规则文件较大，请耐心等待

* 该网站为静态网站，不收集任何用户数据。网页加载完后，导入的数据文件是在本地进行处理，不会通过网络发送数据

* 如果觉得网页打开慢，或者担心信息泄露，可以点击以下链接，下载网页源码，解压后再双击index.html打开页面即可使用（之后无需再访问网络）

## DRG分组器下载（网页版）
https://github.com/OpenDRG/OpenDRG.github.io/archive/refs/heads/main.zip

## 联系开发团队
请发邮件至OpenDRG@hotmail.com
