---
show: step
version: 1.0
enable_checker: true
---

# 类型提示(type hint)

## 回忆

- 我们上次了解了字典作为参数
- 字典作为形参(args)被定义
	- 如果实参传过来是多个元素
		- 形式是关键字型
		- 用逗号隔开
		- 函数中可以用对kwargs解包
		- kwargs是一个字典
	- 这样我们就可以在调用的时候使用不定长的字典参数了
	- 这也很方便
- 字典作为实参被调用的时候
	- 如果真的是一个字典变量	
		- 前面要加上**
		- 变成**kwargs
		- 可以把字典项作为参数一个个传过去
- 函数还有什么好玩的？

### *作用

- 可以把容器对象中的内容	
	- 从容器中释放出来

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221027-1666859077227)

- 只是容器类的对象吗？

### 可迭代对象

- 容器类对象本质上都是可迭代的
	- iterable的

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221027-1666859174887)

- 从可迭代对象中释放出来的元素
	- 还可以和其他元素进行组合吗？

### 重新组合

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221027-1666859375766)

- *t可以把t中的元素列出来
	- *t, 3可以得到一个新的元组

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221027-1666859423602)

- *l 可以列出列表中的所有元素

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221027-1666859452411)

- 这种东西可以进行赋值吗？

### 赋值

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221027-1666861840828)

- 逗号会把一些变量自动封装成元组
	- 赋值的时候会自动解包
- 其实
	- 我们函数的实参也是被自动封成元组
	- 然后自动解包的
- 得到的l 是一个列表

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221027-1666861783843)

- 得到的列表可以转化为元组
- 集合会如何呢？

### 集合

- * 也会列出集合中所有的元素

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221027-1666859558319)

- 得到一个元组
	- 然后可以再将元组转化为集合
- 字典对象可以用*吗？

### 字典对象

- 字典本质上是key-value pair的集合

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221027-1666859696275)

- * 可以把字典中的key遍历出来
	- 然后和其他元素组合
- 如果想要把key 和 value都解包出来呢？

### 解包字典

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221027-1666862135680)

- 两个参数可以把字典中的key和value都解出来
- 然后用大括号括起来得到一个字典
- 或者和其他名值对构成字典
- 如果是两个字典
- 可以用这种方法求和吗？

### 字典求和

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221027-1666862255660)

- 实践验证
- 确实是可以的

### 总结
- 我们这次研究了`*` 和 `**`运算符
- * 可以解包可迭代(iterable)对象
	- 列表
	- 元组
	- 集合
	- range
	- 在赋值的时候
		- * 可以起到不定长列表的作用
- ** 可以解包字典
	- 这样就可以对于字典进行运算
	- 合并
	- 等等操作
- 函数可以接受不同的参数吗？？🤔
- 我们下次再说👋