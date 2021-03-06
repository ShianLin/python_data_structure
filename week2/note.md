# 什么是算法分析
1. 算法：是对问题解决的分步描述【逻辑层面】
程序则是采用某种编程语言实现的算法，同一个
2. 程序：算法通过不同的程序员采用不同的编程语言，能产生很多程序【物理层面】
3. 比较程序的“好坏”，有更多因素：代码风格、可读性等等
4. 我们主要感兴趣的是算法本身特性
5. 算法分析主要就是从计算资源（执行时间、存储空间）消耗的角度来评判和比较算法。更高效利用计算资源，或者更少占用计算资源的算法，就是好算法
6. 但是不同的编程语言和程序，会导致执行时间不同，因此使用时间复杂度来衡量
***
# 大O表示法
1. 一个算法所实施的操作数量或步骤数可作为
独立于具体程序/机器的度量指标
* 使用哪种操作来衡量？
==>需要一种通用的基本操作来作为运行步骤的计量单位
2. 使用赋值语句作为衡量指标
* 因为同时包含了（表达式）计算和（变量）存储
* 控制流语句（顺序、决策和循环）只是组织语句，本身不实行处理
* 定义语句与计算资源无关
3. 问题规模影响算法执行时间。算法分析的目标是找出问题规模怎么影响一个算法的执行时间
4. 数量级函数描述了基本操作数量函数T(n)中**随着n增加而增加速度最快**的主导部分。称作“大O”表示法，记作O(f(n))，其中f(n)表示T(n)中的主导部分。也就是看n的情况
5. 某些具体数据也会影响算法运行时间，因此分为最好、最差和平均的情况。平均情况是算法的主流性能。
6. 
![shuliangji](./img/1.png)
7. 大O表示法:所有上限中最小的上限
8. 大$\Omega$表示法：所有下限中最大的下限
9. 大$\Theta$表示法：如果上下限相同
![shuliangji](/img/2.png)
***
# 变位词的判断问题
1. 变位词两个次之间存在组成字母的重新排列关系,eg.heart和earth
2. 这个是举例子来计算
***
# python数据类型的性能
1. list和dict
* 列表是随机访问的，取值赋值的时间是O(1)
* 列表增加，append是O(1)，列表链接是O(n+k)。n是原列表长度，k是新列表长度
* 列表判断in 是O(n),dic是O(1)
***
# 如何做OJ
1. 输出必须一致，包括看不见的空格
2. 如何做
* 看清题
* 看清样例的格式
a. 多行输入：每行一个```input()```，根据要求转换。若每行一个整数```a = int(input())```
b. 单行输入多个变量，用```input().split()```读入并分解为列表 
c. 多个整数在一行```list(map(int,input().split()))```
d. 多行输出：```print```
e. 浮点数指定：看清保留小数点后几位，用```print('%.3f'%(a/b))```来规定
* 编写程序与测试
* 提交测评