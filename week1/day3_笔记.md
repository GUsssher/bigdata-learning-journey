[#day3_data_structures.py](https://github.com/user-attachments/files/27643764/day3_data_structures.py)今日复习了for循环，列表和字典
在GitHub搜索了awesome data engineering
找到了一份资源清单：https://github.com/DataExpert-io/data-engineer-handbook
查看了里面的project文件中的一个YouTube的教程
大概是教学的，题目是Uber Data Analytics | End-To-End Data Engineering Project，看不懂
今日代码：
#day3_data_structures.py
#===============列表（List）: 有序的箱子================
#场景：从100个传感器每分钟接收一次温度数据
#原始数据就是一串数字，顺序极其重要
temperature_list = [22.5, 23.0, 21.8, '错误', 24.1, 22.9]  #这是一个列表
print(f"原始温度数据箱: {temperature_list}")

#数数有几个数据
print(f"温度数据的数量: {len(temperature_list)}个数据点")
#把“错误”这个脏数据找出来清洗
#先遍历列表
clean_list = []
for temp in temperature_list:
    try:
        num_temp = float(temp)  #如果这个数据是数字类型
        clean_list.append(num_temp)  #如果是数字就放到新的干净列表里
    except:
        print(f"发现脏数据: {temp}")
print(f"清洗后的温度数据: {clean_list}")
#计算平均温度（常常考试手写）
average_temp = sum(clean_list) / len(clean_list)
print(f"平均温度: {average_temp:.2f}°C")
#===============字典（Dict）: 贴标签的箱子================
#场景：每个传感器除了温度数据还有湿度，电压和位置
#原始数据是一个个标签和对应的数值
sensor_1_data = {
    "设备ID": "sensor_001",
    "温度": 22.5,
    "湿度": "60.0%",
    "电压": 3.3,
    "位置": "山东日照404",
    "在线状态": True,
}
#从字典取值
print(f"传感器ID: {sensor_1_data['设备ID']}的位置在{sensor_1_data['位置']}")
#清洗脏数据
raw_humidity = sensor_1_data["湿度"]  #这是一个字符串" 60.0%"
clean_humidity = float(raw_humidity.replace("%", ""))  #去掉空格和百分号，转换成数字
sensor_1_data["湿度"] = clean_humidity  #把清洗后的数字放回字典里
print(f"清洗后的传感器完整信息: {sensor_1_data}")
