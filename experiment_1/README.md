# 直方图均衡
- 直方图均衡化处理后，图像可以达到增强的效果  
- 有很多的方式来执行均衡化，从而得到不同的结果。请考虑和尝试更多的方法并且比较你尝试的方法的结果。
- 要求：不允许使用 matlab 中的 histeq 函数。允许使用其他程序语言如python, c++实现(只需一种即可），但是不可以调用涉及核心算法的相关函数，当然，你可以使用这些方法与你的结果进行对比。

## 数据
- data/lena.jpg

## 实验脚本
- hist.py

## 公式
- 直方图均衡化算法:
1. 统计图象中各灰度级像素个数$n_k$; 
2. 计算直方图中应变量的值:$p_k=n_k/(M×N)$;
3. 计算累计直方图中应变量的值:$S_k=\sum p_k$;
4. 取整$S_k=int\{(L-1)S_k\}$;
5. 确定映射对应关系:$k\rightarrow S_k$;
6. 对图象进行增强变换$( k\rightarrow S_k)$.   
 
其中L是灰度层次数， M×N是图幅参数