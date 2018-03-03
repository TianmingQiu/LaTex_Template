# Code Notes
## C++
- for 循环里的语句顺序不要写错！自增在最后一个！`for (int n = 0; n < 0; n++){} `.
- vector添加新元素：`.push_back(new element)`，并且，初始化的时候无法直接赋很多

## Python
- Python的for循环：` for j in range(i + 1, len(nums)):`. range的起始点可以不是0.
- 返回2D list的维数：
```
>>> array = [[1,2],[3,4],[5,6]]
>>> len(array)
3
>>> len(array[0])
2
```
- 在类中调用其他的成员函数，得加`self.`
- 在写递归调用函数时，每一步的输出也要相同，比如在写那个BinarySearch的时候：BoolResult = BinarySearch（t， a），最后在总的return BoolResult
