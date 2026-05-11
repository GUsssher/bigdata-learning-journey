又一次尝试了代码编写，晚自习把之前学过的基础全部复习了一遍
其中包括了各种基础代码含义
大数据工程师清洗数据时间长，因为大数据收集信息过多，且大部分数据信息为“脏数据”包含各种格式和语言等等
收集了一些基础的“方法”
列表：
append(x)	在末尾追加一个元素
extend(iterable)	用可迭代对象的所有元素扩展列表
insert(i, x)	在索引 i 处插入元素
remove(x)	删除第一个值为 x 的元素，不存在则报错
pop([i])	删除并返回索引 i 的元素（默认最后一个）
clear()	清空列表
index(x[, start[, end]])	返回第一个值为 x 的索引，不存在则报错
count(x)	统计 x 出现的次数
sort(key=None, reverse=False)	对列表进行原地排序
reverse()	原地反转列表顺序
copy()	返回列表的浅拷贝
字符串：
lower() / upper()	全转小写 / 全转大写
strip([chars])	去除两端指定字符（默认空白）
lstrip() / rstrip()	只去除左端 / 右端
split(sep=None)	按分隔符分割成列表，默认按空白分割
join(iterable)	用字符串连接可迭代对象中的字符串
replace(old, new[, count])	替换子串
find(sub) / index(sub)	查找子串，find 找不到返回 -1，index 报错
startswith(prefix) / endswith(suffix)	判断是否以指定字符串开头/结尾
count(sub)	统计子串出现次数
format(*args, **kwargs)	格式化字符串
isdigit() / isalpha() / isalnum() / isspace()	判断字符类型
splitlines()	按换行符分割成列表
capitalize() / title() / swapcase()	首字母大写 / 每个单词首字母大写 / 大小写交换
字典：
keys()	返回所有键的视图（可迭代）
values()	返回所有值的视图
items()	返回所有 (键, 值) 对的视图
get(key[, default])	获取键的值，键不存在时返回 default（不报错）
pop(key[, default])	删除键并返回值，若不存在且无 default 则报错
popitem()	删除并返回最后插入的键值对（Python 3.7+ 有序）
update([other])	用另一个字典或键值对更新原字典
setdefault(key[, default])	若键存在返回值，否则设置键为 default 并返回它
clear()	清空字典
copy()	浅拷贝
