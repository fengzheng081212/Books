# Grammar

#### \_\_init\_\_

注意到\_\_init\_\_方法的第一个参数永远是self，表示创建的实例本身，因此，在\_\_init\_\_方法内部，就可以把各种属性绑定到self，因为self就指向创建的实例本身。有了\_\_init\_\_方法，在创建实例的时候，就不能传入空的参数了，必须传入与\_\_init\_\_方法匹配的参数，但self不需要传，Python解释器自己会把实例变量传进去

#### 私有变量

在Python中，实例的变量名如果以"\_\_"开头，就变成了一个**私有变量**（private），只有内部可以访问，外部不能访问

私有变量可以通过以下方式被外部变量访问和修改：

```python
class Student(object):
    ...

    def get_name(self):
        return self.__name
        
    def get_score(self):
        return self.__score
        
    def set_score(self, score):
        self.__score = score
```

#### list

list是一种有序的集合，可以随时添加和删除其中的元素。

#### tuple

tuple和list非常类似，但是tuple一旦初始化就不能修改

#### dic

dict全称dictionary，在其他语言中也称为map，使用键-值（key-value）存储，具有极快的查找速度。

```python
>>> d = {'Michael': 95, 'Bob': 75, 'Tracy': 85}
>>> d['Michael']
95
```

#### set

set和dict类似，也是一组key的集合，但不存储value。由于key不能重复，所以，在set中，没有重复的key。

```python
>>> s = set([1, 1, 2, 2, 3, 3])
>>> s
{1, 2, 3}
```

#### lambda

 关键字`lambda`表示匿名函数，冒号前面的`x`表示函数参数

匿名函数`lambda x: x * x`实际上就是：

```python
def f(x):
    return x * x
```

**实例属性和类属性**

实例属性属于各个实例所有，互不干扰；

类属性属于类所有，所有实例共享一个属性；

不要对实例属性和类属性使用相同的名字，否则将产生难以发现的错误。

