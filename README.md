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
|-|-|CHS-DRG 1.2|2024年|634组|是|[chs_drg_12](https://opendrg.github.io?type=chs_drg_12)|
|-|-|CHS-DRG 1.1|2023年|628组|是|[chs_drg_11](https://opendrg.github.io?type=chs_drg_11)|
|-|-|CHS-DRG 1.0|2022年|618组|是|[chs_drg_10](https://opendrg.github.io?type=chs_drg_10)|
|四川|全省统一|CHS-DRG 1.2|2024年|753组|是|[sichuan_2024](https://opendrg.github.io?type=sichuan_2024)|
|北京|-|CHS-DRG 1.1|2022年|696组|是|[beijing_2022](https://opendrg.github.io?type=beijing_2022)|
|上海|-|CHS-DRG 1.1|2023年|1039组|是|[shanghai_2023](https://opendrg.github.io?type=shanghai_2023)|
|天津|-|CHS-DRG 1.1|2024年|696组|是|仅专业版支持|
|重庆|-|CHS-DRG 1.1|2024年|880组|是|[chongqing_2024](https://opendrg.github.io?type=chongqing_2024)|
|浙江|-|ZJ-DRG 1.1|2022年|1006组|是|仅专业版支持|
|广西|-|CHS-DRG 1.1|2022年|984组|是|[guangxi_2022](https://opendrg.github.io?type=guangxi_2022)|
|云南|-|CHS-DRG 1.1|2023年|762组|是|仅专业版支持|
|江苏|南京|CHS-DRG 1.1|2023年|935组|是|[nanjing_2022](https://opendrg.github.io?type=nanjing_2022)|
|江苏|盐城|CHS-DRG 1.1|2023年|628组|否|[yancheng_2023](https://opendrg.github.io?type=yancheng_2023)|
|江苏|苏州|CHS-DRG 1.1|2023年|667组|是|[suzhou_2023](https://opendrg.github.io?type=suzhou_2023)|
|江苏|泰州|CHS-DRG 1.1|2023年|760组|是|[taizhou_2023](https://opendrg.github.io?type=taizhou_2023)|
|江苏|无锡|CHS-DRG 1.1|2023年|611组|是|[wuxi_2023](https://opendrg.github.io?type=wuxi_2023)|
|江苏|常州|CHS-DRG 1.1|2023年|667组|是|[changzhou_2023](https://opendrg.github.io?type=changzhou_2023)|
|江苏|南通|CHS-DRG 1.1|2022年|603组|是|[nantong_2022](https://opendrg.github.io?type=nantong_2022)|
|江苏|徐州|CHS-DRG 1.1|2023年|959组|是|[xuzhou_2023](https://opendrg.github.io?type=xuzhou_2023)|
|山东|济南|CHS-DRG 1.1|2022年|887组|否|[jinan_2023](https://opendrg.github.io?type=jinan_2023)|
|山东|临沂|CHS-DRG 1.1|2023年|628组|否|[linyi_2023](https://opendrg.github.io?type=linyi_2023)|
|山东|青岛|CHS-DRG 1.1|2023年|682组|是|[qingdao_2023](https://opendrg.github.io?type=qingdao_2023)|
|山东|聊城|CHS-DRG 1.1|2022年|683组|是|[liaocheng_2022](https://opendrg.github.io?type=liaocheng_2022)|
|山东|烟台|CHS-DRG 1.1|2023年|647组|是|[yantai_2023](https://opendrg.github.io?type=yantai_2023)|
|福建|福州|CHS-DRG 1.1|2022年|563组|是|[fuzhou_2022](https://opendrg.github.io?type=fuzhou_2022)|
|福建|南平|CHS-DRG 1.1|2023年|795组|是|[nanping_2023](https://opendrg.github.io?type=nanping_2023)|
|福建|泉州|CHS-DRG 1.1|2023年|612组|是|[nanping_2023](https://opendrg.github.io?type=quanzhou_2023)|
|福建|省医保|CHS-DRG 1.1|2023年|656组|是|[fujian_2023](https://opendrg.github.io?type=fujian_2023)|
|陕西|西安|CHS-DRG 1.1|2021年|628组|否|[xian_2021](https://opendrg.github.io?type=xian_2021)|
|陕西|铜川|CHS-DRG 1.1|2023年|628组|否|[tongchuan_2023](https://opendrg.github.io?type=tongchuan_2023)|
|陕西|咸阳|CHS-DRG 1.1|2024年|628组|否|仅专业版支持|
|陕西|安康|CHS-DRG 1.1|2023年|654组|是|[ankang_2023](https://opendrg.github.io?type=ankang_2023)|
|贵州|六盘水|CHS-DRG 1.1|2022年|628组|否|[chs_drg_11](https://opendrg.github.io?type=chs_drg_11)|
|贵州|铜仁|CHS-DRG 1.1|2022年|628组|否|[chs_drg_11](https://opendrg.github.io?type=chs_drg_11)|
|四川|成都|CHS-DRG 1.0|2022年|618组|否|[chengdu_2022](https://opendrg.github.io?type=chengdu_2022)|
|四川|宜宾|CHS-DRG 1.1|2023年|749组|是|[yibin_2023](https://opendrg.github.io?type=yibin_2023)|
|四川|资阳|CHS-DRG 1.1|2023年|737组|是|[ziyang_2023](https://opendrg.github.io?type=ziyang_2023)|
|四川|乐山|CHS-DRG 1.1|2023年|664组|是|[leshan_2023](https://opendrg.github.io?type=leshan_2023)|
|四川|内江|CHS-DRG 1.1|2023年|592组|是|仅专业版支持|
|四川|达州|CHS-DRG 1.1|2022年|823组|是|[dazhou_2022](https://opendrg.github.io?type=dazhou_2022)|
|四川|巴中|CHS-DRG 1.1|2023年|593组|是|[bazhong_2023](https://opendrg.github.io?type=bazhong_2023)|
|四川|自贡|CHS-DRG 1.1|2022年|690组|是|仅专业版支持|
|四川|雅安|CHS-DRG 1.1|2021年|665组|是|[yaan_2024](https://opendrg.github.io?type=yaan_2024)|
|四川|绵阳|CHS-DRG 1.1|2023年|776组|是|[mianyang_2023](https://opendrg.github.io?type=mianyang_2023)|
|四川|遂宁|CHS-DRG 1.1|2023年|766组|是|[suining_2023](https://opendrg.github.io?type=suining_2023)|
|四川|广安|CHS-DRG 1.1|2023年|715组|是|[guangan_2023](https://opendrg.github.io?type=guangan_2023)|
|四川|广安扩面|CHS-DRG 1.1|2024年|715组|是|[guangan_2024](https://opendrg.github.io?type=guangan_2024)|
|四川|省医保|CHS-DRG 1.0|2022年|968组|是|[sichuan_2022](https://opendrg.github.io?type=sichuan_2022)|
|湖北|武汉|CHS-DRG 1.0|2024年|660组|是|[wuhan_2024](https://opendrg.github.io?type=wuhan_2024)|
|湖南|长沙市<br>株洲市<br>湘潭市<br>衡阳市|CHS-DRG 1.1|2023年|737组|是|[changsha_2023](https://opendrg.github.io?type=changsha_2023)|
|山西|郴州|CHS-DRG 1.1|2024年|734组|是|[taiyuan_2023](https://opendrg.github.io?type=taiyuan_2024)|
|山西|太原|CHS-DRG 1.1|2023年|593组|是|[taiyuan_2023](https://opendrg.github.io?type=taiyuan_2023)|
|山西|长治|CHS-DRG 1.1|2022年|653组|是|[changzhi_2022](https://opendrg.github.io?type=changzhi_2022)|
|山西|临汾|CHS-DRG 1.1|2022年|645组|是|[linfen_2022](https://opendrg.github.io?type=linfen_2022)|
|山西|运城|CHS-DRG 1.1|2023年|690组|是|[yuncheng_2023](https://opendrg.github.io?type=yuncheng_2023)|
|山西|大同|CHS-DRG 1.1|2023年|709组|是|仅专业版支持|
|甘肃|兰州|CHS-DRG 1.1|2023年|794组|是|仅专业版支持|
|甘肃|庆阳|CHS-DRG 1.1|2023年|630组|是|[qingyang_2023](https://opendrg.github.io?type=qingyang_2023)|
|宁夏|银川|CHS-DRG 1.1|2023年|639组|是|[yinchuan_2023](https://opendrg.github.io?type=yinchuan_2023)|
|新疆|乌鲁木齐市|CHS-DRG 1.1|2022年|718组|是|[wlmq_2022](https://opendrg.github.io?type=wlmq_2022)|
|新疆|喀什市|CHS-DRG 1.1|2022年|586组|是|[kashi_2022](https://opendrg.github.io?type=kashi_2022)|
|新疆|生产建设<br>兵团|CHS-DRG 1.1|2022年|635组|是|[xjbt_2022](https://opendrg.github.io?type=xjbt_2022)|
|新疆|克州|CHS-DRG 1.1|2022年|637组|是|[kezhou_2023](https://opendrg.github.io?type=kezhou_2023)|
|黑龙江|哈尔滨|CHS-DRG 1.1|2024年|731组|是|仅专业版支持|
|黑龙江|牡丹江|CHS-DRG 1.1|2023年|593组|是|[mudanjiang_2023](https://opendrg.github.io?type=mudanjiang_2023)|
|吉林|长春|CHS-DRG 1.1|2022年|636组|是|[changchun_2022](https://opendrg.github.io?type=changchun_2022)|
|吉林|吉林|CHS-DRG 1.1|2022年|625组|是|[jilin_2022](https://opendrg.github.io?type=jilin_2022)|
|辽宁|沈阳|CHS-DRG 1.1|2023年|605组|是|[shenyang_2022](https://opendrg.github.io?type=shenyang_2023)|
|辽宁|大连|CHS-DRG 1.1|2022年|646组|是|[dalian_2022](https://opendrg.github.io?type=dalian_2022)|
|辽宁|丹东|CHS-DRG 1.1|2024年|638组|是|仅专业版支持|
|辽宁|鞍山|CHS-DRG 1.1|2022年|579组|是|[anshan_2023](https://opendrg.github.io?type=anshan_2023)|
|河南|安阳|CHS-DRG 1.1|2021年|802组|是|[anyang_2021](https://opendrg.github.io?type=anyang_2021)|
|河南|漯河|CHS-DRG 1.1|2022年|810组|是|[luohe_2022](https://opendrg.github.io?type=luohe_2022)|
|河南|周口|CHS-DRG 1.1|2023年|799组|是|仅专业版支持|
|河南|开封|CHS-DRG 1.1|2024年|831组|是|仅专业版支持|
|河南|驻马店|CHS-DRG 1.1|2023年|615组|是|[zhumadian_2023](https://opendrg.github.io?type=zhumadian_2023)|
|河南|济源|CHS-DRG 1.1|2023年|632组|是|[jiyuan_2023](https://opendrg.github.io?type=jiyuan_2023)|
|广东|佛山|CHS-DRG 1.1|2022年|848组|是|[foshan_2022](https://opendrg.github.io?type=foshan_2022)|
|安徽|合肥|CHS-DRG 1.1|2023年|851组|是|[hefei_2023](https://opendrg.github.io?type=hefei_2023)|
|安徽|六安|CHS-DRG 1.1|2023年|650组|是|[liuan_2023](https://opendrg.github.io?type=liuan_2023)|
|安徽|马鞍山|CHS-DRG 1.1|2022年|552组|是|[maanshan_2022](https://opendrg.github.io?type=maanshan_2022)|
|安徽|蚌埠|CHS-DRG 1.1|2023年|641组|是|[bengbu_2023](https://opendrg.github.io?type=bengbu_2023)|
|河北|邯郸|CHS-DRG 1.1|2024年|619组|是|[handan_2022](https://opendrg.github.io?type=handan_2024)|
|江西|南昌|CHS-DRG 1.1|2023年|825组|是|[nanchang_2023](https://opendrg.github.io?type=nanchang_2023)|
|青海|西宁|CHS-DRG 1.0|2023年|622组|是|[xining_2023](https://opendrg.github.io?type=xining_2023)|

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

商务合作或售后支持可联系以下成员：

宁老师 13796827827 （黑龙江）
袁老师 13880298762 （四川）
段老师 15020135300 （山东）
闫晓伟 19339880181 （河南）
张家玮 18919032822 （甘肃、青海）
璞玉 微信puyu-co （陕西）
雒老师 13602127269 （天津）
陈良 15108208024 （重庆）
王永 15974684985 （云南）

其余区域的合作，或软件技术问题讨论交流，请发邮件至OpenDRG@hotmail.com