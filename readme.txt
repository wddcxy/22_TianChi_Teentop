队伍名称：邵宗杰
联系方式：wddcxy@126.com (电子邮箱)
线上排名：22
成绩：20.81

解题思路：
先把数据按照5分钟粒度切分，
再根据pti（故障时间-日志时间）把数据分成6种，（无故障，4、8、12、16、20分钟内故障），
丢弃最小pti（单机器所有pti中最小的）大于1200的离群点，
用多分类的方法解决问题。模型采用的是lightgbm。

参考说明：
参考了示例代码，在示例代码的基础上，为了让pti更细致，将类别从4种提升到了6种。模型从xgboost换成了lightgbm

目录结构：
- my_submission
| - __init__.py
| - main.ipynb # 训练模型代码
| - requirements.txt # python软件包说明
| - submission.ipynb # 预测结果代码
| - supplements/ #存放模型文件及数据集
| - data.py # 存放各种路径（模型文件路径，输出结果路径......）

软件环境：
python版本 3.9.9
系统版本	Windows 10 专业版
系统版本号	21H2
（python软件包及版本请见requirements.txt）

硬件环境：
本地训练使用机器配置64位4核4G笔记本，未使用GPU
