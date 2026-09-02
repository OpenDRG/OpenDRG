# OpenDRG的目标是成为国家医保局CHS-DRG的开源实现，就像OpenJDK是Java SE的开源实现一样

## 官方网站上线&emsp;[OpenDRG.cn](https://opendrg.cn/)

新的分组器演示平台，访问更快：[demo.OpenDRG.cn](https://demo.opendrg.cn/)

![image](https://www.opendrg.cn/opendrg_banner.jpg)
![image](https://www.opendrg.cn/opendrg_home.jpg)

## 业务背景

&emsp;&emsp;疾病诊断相关组（Diagnosis Related Groups，DRG）是用于衡量医疗服务质量效率以及进行医保支付的重要工具。国家医保局已经出台文件，要求从2022到2024年，三年内全面完成DRG/DIP付费方式改革，很多省市医保局已经采用DRG方式与医院进行结算。医院为了应对DRG支付改革，需要掌握DRG分组规则。但是各地DRG分组规则不统一，经常变化，医院很难通过自行研究去掌握。如果花高价去采购商业DRG软件，一方面软件厂商在各地规则的研究方面，水平参差不齐，很多时候不能及时满足需求；另一方面，大部分厂商的软件是封闭式的，医院不能自由的调用底层分组接口或者进行二次开发，尤其很难满足大批量数据分析方面的需求。

&emsp;&emsp;我们一批志同道合的的小伙伴，花费大量时间精力，学习DRG理论、研究国家DRG政策、跟踪各省市的DRG改革进程，并且研发了DRG分组器软件，在一些地区成功实践。为了帮助更多的医院解决DRG难题，助力国家DRG改革，我们在“开放源代码软件”运动的启发下，决定按照“开放、透明、协作、交付”的原则，向全国的医院免费提供OpenDRG分组器源代码，并欢迎所有的信息化厂商进行集成。

## OpenDRG分组器产品优势
* 严格按照医保局规则进行分组，其正确性经过多个地区、多家医院的实际验证
* 以插件方式嵌入医院业务系统运行，不需要部署服务器，不增加医院服务器负担
* 采用Java、C#、python、js等多种语言实现，方便医院HIS、EMR、病案等不同技术架构的系统来集成
* 性能非常高，5000份病案的分组，最多只要1秒钟，即满足日常业务处理，也能应用到大数据分析场景
* 采用开源方式运作，很多业内有志之士提供支持，不管是分组规则还是软件功能，都更新非常快
* 提供免费版本，可供医疗机构永久免费使用

## 各地方分组方案支持情况
|省份|城市|DRG基础版本|更新年度|DRG组数|本地化<br>细分组|测试链接|
|-|-|-|-|-|-|-|
|-|-|CHS-DRG 3.0|2026年|825组|是|[chs_drg_30](https://opendrg.github.io?type=chs_drg_30)|
|-|-|CHS-DRG 2.0|2024年|634组|是|[chs_drg_20](https://opendrg.github.io?type=chs_drg_20)|
|-|-|CHS-DRG 1.2|2024年|634组|是|[chs_drg_12](https://opendrg.github.io?type=chs_drg_12)|
|-|-|CHS-DRG 1.1|2023年|628组|是|[chs_drg_11](https://opendrg.github.io?type=chs_drg_11)|
|-|-|CHS-DRG 1.0|2022年|618组|是|[chs_drg_10](https://opendrg.github.io?type=chs_drg_10)|
|北京|-|CHS-DRG 1.1|2024年|682组|是|[beijing_2024](https://opendrg.github.io?type=beijing_2024)|
|上海|-|CHS-DRG 1.1|2023年|1039组|是|[shanghai_2023](https://opendrg.github.io?type=shanghai_2023)|
|天津|-|CHS-DRG 1.1|2024年|696组|是|仅专业版支持|
|重庆|-|CHS-DRG 2.0|2025年|859组|是|仅专业版支持|
|浙江|-|CHS-DRG 2.0|2024年|953组|是|仅专业版支持|
|广西|-|CHS-DRG 2.0|2024年|653组|是|仅专业版支持|
|云南|-|CHS-DRG 2.0|2024年|681组|是|仅专业版支持|
|江苏|全省统一|CHS-DRG 2.0|2025年|1013组|是|仅专业版支持|
|江苏|南京|CHS-DRG 2.0|2024年|801组|是|[nanjing_2024](https://opendrg.github.io?type=nanjing_2024)|
|山东|全省统一|CHS-DRG 2.0|2024年|675组|是|[shandong_2024](https://opendrg.github.io?type=shandong_2024)|
|山东|临沂|CHS-DRG 1.1|2023年|628组|否|[linyi_2023](https://opendrg.github.io?type=linyi_2023)|
|山东|青岛|CHS-DRG 2.0|2024年|701组|是|[qingdao_2024](https://opendrg.github.io?type=qingdao_2024)|
|山东|聊城|CHS-DRG 1.1|2022年|683组|是|[liaocheng_2022](https://opendrg.github.io?type=liaocheng_2022)|
|山东|烟台|CHS-DRG 1.1|2023年|647组|是|[yantai_2023](https://opendrg.github.io?type=yantai_2023)|
|福建|全省统一|CHS-DRG 2.0|2024年|836组|是|[fujian_2024](https://opendrg.github.io?type=fujian_2024)|
|福建|福州|CHS-DRG 1.1|2022年|563组|是|[fuzhou_2022](https://opendrg.github.io?type=fuzhou_2022)|
|福建|南平|CHS-DRG 1.1|2023年|795组|是|[nanping_2023](https://opendrg.github.io?type=nanping_2023)|
|陕西|西安|CHS-DRG 2.0|2025年|634组|否|[xian_2025](https://opendrg.github.io?type=xian_2025)|
|陕西|铜川|CHS-DRG 2.0|2025年|634组|否|[tongchuan_2023](https://opendrg.github.io?type=tongchuan_2025)|
|陕西|咸阳|CHS-DRG 2.0|2025年|746组|否|仅专业版支持|
|陕西|安康|CHS-DRG 2.0|2025年|724组|是|[ankang_2025](https://opendrg.github.io?type=ankang_2025)|
|贵州|六盘水|CHS-DRG 2.0|2025年|634组|否|[chs_drg_20](https://opendrg.github.io?type=chs_drg_20)|
|贵州|铜仁|CHS-DRG 2.0|2024年|634组|是|[tongren_2024](https://opendrg.github.io?type=tongren_2024)|
|四川|全省统一|CHS-DRG 2.0|2024年|753组|是|仅专业版支持|
|湖北|武汉|CHS-DRG 2.0|2024年|773组|是|[hubei_2024](https://opendrg.github.io?type=hubei_2024)|
|湖南|长沙市<br>株洲市<br>湘潭市<br>衡阳市|CHS-DRG 2.0|2024年|725组|是|[changsha_2024](https://opendrg.github.io?type=changsha_2023)|
|湖南|郴州|CHS-DRG 2.0|2025年|736组|是|[chenzhou_2024](https://opendrg.github.io?type=chenzhou_2025)|
|山西|全省统一|CHS-DRG 2.0|2024年|740组|是|仅专业版支持|
|甘肃|全省统一|CHS-DRG 2.0|2025年|776组|是|仅专业版支持|
|宁夏|银川|CHS-DRG 1.1|2023年|639组|是|[yinchuan_2023](https://opendrg.github.io?type=yinchuan_2023)|
|新疆|全省统一|CHS-DRG 2.0|2024年|765组|是|[xinjiang_2024](https://opendrg.github.io?type=xinjiang_2024)|
|黑龙江|全省统一|CHS-DRG 2.0|2024年|658组|是|仅专业版支持|
|吉林|全省统一|CHS-DRG 2.0|2024年|829组|是|仅专业版支持|
|辽宁|全省统一|CHS-DRG 2.0|2024年|670组|是|仅专业版支持|
|河南|全省统一|CHS-DRG 2.0|2024年|832组|是|仅专业版支持|
|广东|佛山|CHS-DRG 2.0|2025年|802组|是|[foshan_2025](https://opendrg.github.io?type=foshan_2025)|
|安徽|合肥|CHS-DRG 2.0|2025年|759组|是|[hefei_2025](https://opendrg.github.io?type=hefei_2025)|
|安徽|六安|CHS-DRG 1.1|2023年|650组|是|[liuan_2023](https://opendrg.github.io?type=liuan_2023)|
|安徽|马鞍山|CHS-DRG 1.1|2023年|588组|是|[maanshan_2023](https://opendrg.github.io?type=maanshan_2023)|
|安徽|蚌埠|CHS-DRG 1.1|2023年|641组|是|[bengbu_2023](https://opendrg.github.io?type=bengbu_2023)|
|安徽|滁州|CHS-DRG 1.1|2024年|723组|否|[chuzhou_2024](https://opendrg.github.io?type=chuzhou_2024)|
|安徽|池州|CHS-DRG 1.1|2024年|648组|否|[chizhou_2024](https://opendrg.github.io?type=chizhou_2024)|
|河北|邯郸|CHS-DRG 2.0|2025年|738组|是|[handan_2025](https://opendrg.github.io?type=handan_2025)|
|河北|定州|CHS-DRG 1.1|2024年|622组|是|[dingzhou_2025](https://opendrg.github.io?type=dingzhou_2025)|
|江西|南昌|CHS-DRG 2.0|2025年|811组|是|[nanchang_2025](https://opendrg.github.io?type=nanchang_2025)|
|江西|上饶|CHS-DRG 2.0|2025年|629组|是|[shangrao_2025](https://opendrg.github.io?type=shangrao_2025)|
|青海|全省统一|CHS-DRG 2.0|2024年|723组|是|[qinghai_2024](https://opendrg.github.io?type=qinghai_2024)|

&emsp;&emsp;其余地区的分组器正在收集资料和开发，将逐步发布，敬请关注

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

## DRG分组器下载
* 社区版
https://github.com/OpenDRG/OpenDRG.github.io/archive/refs/heads/main.zip
* 专业版
下载本项目下zip文件

## 使用方式

下载解压后打开index.html文件

## 联系团队

医院人士加业务交流群请加微信13801750519，邀请入群
商务合作或售后支持可发邮件至OpenDRG@hotmail.com，或者联系以下成员：

区域 | 成员 | 联系方式 | 备注
--- | --- | --- | ---
云南 | 王永 | 15974684985 |
广西 | 何玉梅  |18978725836 |
陕西 | 璞玉  |puyu-co | 微信号
河南 | 闫晓伟  |19339880181 |
天津 | 雒老师 |13602127269 |
黑龙江 | 宁老师 |13796827827 |
辽宁 | 尚利民  |13322267930 |
山西 | 曹静怡 | 19934941048 |
其他地区 | 高文  |13801750519 |

