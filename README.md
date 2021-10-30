测评:

Part 1 下载A股所有股票历史数据

使用Jupyter Notebook, 从Yahoo Finance上，按照股票代码下载了所有A股股票的全部历史数据。处于加速下载速度的考虑，分为了深证和上证两个部分进行下载。

Part 2 全盘部署定时下载每日最新数据

1. 在文本框中输入希望更新的数据的日期
![image](https://user-images.githubusercontent.com/74880402/139532843-725aec2a-fbce-470f-a6b5-fe23f0c664de.png)

2. 在文本框中输入希望开始更新数据的具体时间
![image](https://user-images.githubusercontent.com/74880402/139533024-2a12bbb6-6980-4007-b4f1-070e7d4d1533.png)

Part 3 使用Jupyter Notebook进行分析

1. 针对所有A股进行分析

   对所有深证上证股票进行了简单的聚合分析，分别对Open, Close, High, Low, Volume进行了简单的聚合运算，
   
   结果如下
	 
	 1.上证：
	 
	 ![image](https://user-images.githubusercontent.com/74880402/139531970-5e277759-1ee0-43b7-abc8-20b397bc9996.png)
	 
	 2.深证：
	 
	 ![image](https://user-images.githubusercontent.com/74880402/139531997-5d8b7cdc-f5a1-494d-9ca4-8c43cd956f62.png) 
	 
2. 针对个股进行分析（紫金矿业 2020/10 – 2021/10）

	![image](https://user-images.githubusercontent.com/74880402/139532076-ae7d3df7-e065-4e0f-9f6e-f8c8e81e996b.png)
	
	1. 紫金矿业开盘价与收盘价走势
	
	![image](https://user-images.githubusercontent.com/74880402/139532108-d5e091b1-318e-4e47-82bb-e8bc633f1002.png)
	
	2. 紫金矿业高价与低价走势
	
	![image](https://user-images.githubusercontent.com/74880402/139532117-a4ab6236-8965-4ddc-9560-df364aa0a09a.png)
	
	3. 紫金矿业收盘价跌涨走势
	
	![image](https://user-images.githubusercontent.com/74880402/139532121-0d68d1fc-9dea-4b97-b82e-ad962d068fef.png)
	
	4. 紫金矿业50/100/150/200日MA
	
	![image](https://user-images.githubusercontent.com/74880402/139532130-efc6fba5-f6c6-4f42-b263-67698465cb72.png)
	
	5. 紫金矿业布林带（mean(40日)，var(20日)）
	
	![image](https://user-images.githubusercontent.com/74880402/139532173-447ce3d1-3182-4f23-9e2f-c23971dd5fe5.png)
	
3. 针对随机三只股票进行分析（恒瑞医药，复星医药，中国医药 2019/10 – 2021/10）

	1. 三只股票的相关性
	
	![image](https://user-images.githubusercontent.com/74880402/139532188-77e31c72-eceb-4853-a184-d5a85732ca8d.png)
	
 	2. 三只股票的Returns比较
 	
 	![image](https://user-images.githubusercontent.com/74880402/139532200-31dae4d4-e897-4cac-841e-4548b36b5f1b.png)
	![image](https://user-images.githubusercontent.com/74880402/139532217-af06b985-46d6-48a8-a510-19fd244f5769.png)
	
	3. 三只股票Returns的相关性
	
	![image](https://user-images.githubusercontent.com/74880402/139532222-f7e60bcb-11c6-4f05-a1b9-16c5e520fe6c.png)
	
	4. 三只股票从2019/10至2021/10的累积回报
	
	![image](https://user-images.githubusercontent.com/74880402/139532242-310d6553-09bd-4fdb-ad67-d270cfe8372e.png)
	
4. 针对多只股票进行聚类分析

	1. 随机挑选六只股票：西部矿业，紫金矿业，招商银行，交通银行，复星医药，三元股份。
	
	2. 使用Ski-learn对六只股票聚类分析。
	
	![image](https://user-images.githubusercontent.com/74880402/139532275-07cbd67d-c50b-438a-ba08-c91c0c90dc3f.png)
	
	六只股票可分为两个Cluster（如上图）
	
	Cluster 1: 西部矿业，紫金矿业，复星医药，三元股份
	Cluster 2: 招商银行，交通银行
	
	说明：西部矿业，紫金矿业，复星医药，三元股份这四只股票更为相似
	
	招商银行，交通银行这两只股票更为相似
