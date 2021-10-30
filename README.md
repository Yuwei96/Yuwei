测评:

Part 1 下载A股所有股票历史数据

使用Jupyter Notebook, 从Yahoo Finance上，按照股票代码爬取了所有A股股票的全部历史数据（从1995至2021）。出于加快下载速度的考虑，下载数据主要分为了深证和上证两个部分进行。

Part 2 部署实盘定时下载每日数据

同样出于加快下载速度的考虑，氛围上证和深证两个部分进行

1. 在文本框中输入希望更新的数据的日期
![image](https://user-images.githubusercontent.com/74880402/139532843-725aec2a-fbce-470f-a6b5-fe23f0c664de.png)

2. 在文本框中输入希望开始更新数据的具体时间（具体时间及频率可在文件中进一步修改）
![image](https://user-images.githubusercontent.com/74880402/139533024-2a12bbb6-6980-4007-b4f1-070e7d4d1533.png)

3. 输入后运行即可更新全部数据

Part 3 使用Jupyter Notebook进行分析

1. 针对所有A股进行分析


   对所有深证上证股票进行了简单的聚合分析，分别对高开低收价格以及成交量进行了简单的聚合运算， 
   
   结果如下
	 
	 1.上证：
	 
 	 ![image](https://user-images.githubusercontent.com/74880402/139535822-4a9cfec3-cbbe-4e68-a937-6168f65b8773.png)
	 
	 2.深证：
	 
	 ![image](https://user-images.githubusercontent.com/74880402/139535596-f6873919-d46d-4561-9ebf-f7e69af5d8e9.png)
	 
	 
2. 针对个股进行分析（紫金矿业 2020/10 – 2021/10）

	![image](https://user-images.githubusercontent.com/74880402/139534242-3b414280-0eaa-4af5-816c-08b5390b3652.png)

	
	1. 紫金矿业开盘价与收盘价走势
	
	![image](https://user-images.githubusercontent.com/74880402/139533978-1a7b962e-a3a5-4de9-8070-71a4314bb46f.png)

	2. 紫金矿业高价与低价走势
	
	![image](https://user-images.githubusercontent.com/74880402/139534005-9b1b9bc7-7f79-425b-9a4e-b73c85f531fd.png)

	
	3. 紫金矿业收盘价跌涨走势
	
	![image](https://user-images.githubusercontent.com/74880402/139534038-08a18ea5-b955-4f54-b73f-5837c59625d1.png)

	4. 紫金矿业50/100/150/200日MA

	![image](https://user-images.githubusercontent.com/74880402/139534056-64244863-08f7-47a9-8d5a-c5d8f4b6ba90.png)

	5. 紫金矿业布林带（mean(40日)，sd(20日)）
	
	![image](https://user-images.githubusercontent.com/74880402/139534082-4165e46c-5f63-427a-8662-a2fac9e2e2b6.png)

	
3. 针对随机三只股票进行分析（恒瑞医药，复星医药，中国医药 2019/10 – 2021/10）

	1. 三只股票的相关性
	
	![image](https://user-images.githubusercontent.com/74880402/139534103-0e5b8f6f-13fd-48ac-a97d-7c841e2bb11d.png)

 	2. 三只股票的Returns比较
 	
 	![image](https://user-images.githubusercontent.com/74880402/139534119-2b195e69-324c-4754-ac86-a4c8537d1428.png)
	
	![image](https://user-images.githubusercontent.com/74880402/139534132-eff76e52-d9ab-4f2e-9e33-58d820e90549.png)

	3. 三只股票Returns的相关性
	
	![image](https://user-images.githubusercontent.com/74880402/139534161-e3efa3fd-61b3-4222-9fa1-a0b1397b20e6.png)

	4. 三只股票从2019/10至2021/10的累积回报
	
	![image](https://user-images.githubusercontent.com/74880402/139534170-4be209d0-df0b-4d03-bb02-77df11c8ccc5.png)

4. 针对多只股票进行聚类分析

	1. 随机挑选六只股票：西部矿业，紫金矿业，招商银行，交通银行，复星医药，三元股份。
	
	2. 使用scikit-learn对六只股票聚类分析。
	
	![image](https://user-images.githubusercontent.com/74880402/139532275-07cbd67d-c50b-438a-ba08-c91c0c90dc3f.png)
	
	六只股票可分为两个Cluster（如上图）
	
	Cluster 1: 西部矿业，紫金矿业，复星医药，三元股份
	
	Cluster 2: 招商银行，交通银行
	
	说明：西部矿业，紫金矿业，复星医药，三元股份这四只股票更为相似
	
	招商银行，交通银行这两只股票更为相似
