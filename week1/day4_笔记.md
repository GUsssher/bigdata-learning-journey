今日学习有些困难，遇见了报错和不明白的代码
pathlib是一个工具箱，path是里面一个重要的工具，for import的作用就是把path从pathlib中拿出来，
通用：for-import这一段代码的意思就是将一个工具一段代码从另一个工具箱/代码库中里拿出来。
pathlib是负责解决文件系统路径这一相关问题的工具箱，path是其中的一个工具作用是把路径变成一个可以在python中操作的对象
#  input_file = Path("./week1/test_log.txt")
#  output_file = Path("./week1/clean_data.txt")
#  with open(input_file, "r", encoding="utf-8") as f_in:
#  with open(output_file, "w", encoding="utf-8") as f_out:
#  for line_num, line in enumerate(f_in, start=1):
enumerate = 遍历 + 编号，
start=1 让编号从 1 起
input_file：存放输入文件的路径字符串。这里指向当前目录下 week1 文件夹里的 test_log.txt，它是一个原始日志文件，等着读取和分析。
output_file：存放输出文件的路径字符串。指向同一个 week1 文件夹里的 clean_data.txt，这是处理完数据后，准备写入结果的“干净文件”。
f_in 和 f_out 不是存字符串的容器，它们是“文件对象”（也叫文件句柄），是连接程序和磁盘文件的管道。
for line in f_in 之所以能工作，是因为文件对象是一个可迭代器。它不会一次性把所有内容读到内存，而是在每次迭代时，临时从磁盘读一行出来放入 line 变量，用完即丢弃，继续读下一行。
类似地，f_out.write(...) 是把字符串通过管道立即送进磁盘文件，不是先全部囤在 f_out 里。
##############################
报错：FileNotFoundError: [Errno 2] No such file or directory: 'week1\\test_log.txt'
Python 在告诉你：它在当前的工作目录里，找不到 week1\test_log.txt，也就是路径问题
解决方法：，用 Path(__file__).resolve().parent 锚定脚本位置，
