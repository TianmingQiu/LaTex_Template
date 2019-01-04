## ICP Algo(Iterative Closest Point迭代最近点算法)
#### Aim: 将检测到的点配准到**目标**点云上去
#### I. 初始化 **R**&**T** (TransformationEstimationSVD)
#### II. Iteration:
1. 对于**X**中的每一个点，用当前的**R**和**T**变换到**Y'** 中，在目标点云**Y**中找与**Y'** 最近的点(比如欧式距离)，然后**X**和**Y**中的点就形成了对应关系
2. 当N个点都找到配对时，又可以得到N个：y=**R**x+**T**的方程，用最小二乘法，通过使残差最小化，重新得到一组新的**R**、**T**。
3. 迭代，回到step2.1，直至残差小于一个阈值。

## [Bayesian Regression](https://blog.csdn.net/daunxx/article/details/51725086#%E5%8E%9F%E6%96%87%E5%9C%B0%E5%9D%80)
- 搞清极大似然和极大后验
- 这里需要说明，虽然从公式上来看 MAP=ML∗p(θ)，但是这两种算法有本质的区别，ML将θ视为一个确定未知的值，而MAP则将θ视为一个随机变量。  

