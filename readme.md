# 代码及功能：
## PI_besttag.py
功能：用于对带有个人信息的口令集进行最优个人信息匹配。
输入：fin为带有PI的输入文件路径
输出：fout为每个口令的最优匹配表示方式

## rf_personal_noascii_montecarlo.py
功能：用于进行随机森林的基于个人信息的定向攻击算法的训练+montecarlo模拟实验。
输入：训练集是pin，为使用PI_besttag.py进行最优匹配后的输出文件。测试集是testfile，为原始的带有PI的口令集
输出：fout为随机抽样的路径，gout为模拟攻击结果，格式为口令\t估计猜测数

## rf_personal_new_noasciifeature.py
功能：用于进行随机森林的基于个人信息的定向攻击算法的训练+实际生成猜测的实验。
输入：训练集是pin，为使用PI_besttag.py进行最优匹配后的输出文件。
输出：fout为生成猜测的文件路径

运行时，先对带有PI的数据集运行python PI_besttag.py，输出匹配后的表示方式文件。然后把表示方式文件路径输入到rf_personal_noascii_montecarlo.py或rf_personal_new_noasciifeature.py的代码中，再运行python 代码名即可。注意修改输入输出的文件路径。
###########################################

# 相关科研项目、论文：
毕设的一部分，尚未发表，学术界并未相关论文。主要目的是为了更好地匹配个人信息的使用行为，提高破解率。

# 实验设计：
详见毕业设计第三章的两个实验部分

# 环境
python2.7
sklearn
内存最好大于64G，处理器支持多线程

# 代码实现的关键算法
个人信息行为的最优匹配算法PI_besttag.py以及基于随机森林的定向攻击算法的montecarlo版本和实际生成猜测版本