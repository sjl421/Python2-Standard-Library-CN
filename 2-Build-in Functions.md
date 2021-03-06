# 2.内置函数

Python解释器包含了很多内置函数，如下表所示(按字母顺序)。

<table>
  <thead>
	<tr style="background:gray">
		<th colspan="5">内置函数</th>
	</tr>
  </thead>
  <tbody>
	<tr>
		<td>abs()</td>
		<td>divmod()</td>
		<td>input()</td>
		<td>open()</td>
		<td>staticmethod()</td>
	</tr>
	<tr>
		<td>all()</td>
		<td>enumerate()</td>
		<td>int()</td>
		<td>ord()</td>
		<td>str()</td>
	</tr>
	<tr>
		<td>any()</td>
		<td>eval()</td>
		<td>isinstance()</td>
		<td>pow()</td>
		<td>sum()</td>
	</tr>
	<tr>
		<td>basestring()</td>
		<td>execfile()</td>
		<td>issubclass()</td>
		<td>print()</td>
		<td>super()</td>
	</tr>
	<tr>
		<td>bin()</td>
		<td>file()</td>
		<td>iter()</td>
		<td>property()</td>
		<td>tuple()</td>
	</tr>
	<tr>
		<td>bool()</td>
		<td>filter()</td>
		<td>len()</td>
		<td>range()</td>
		<td>type()</td>
	</tr>
	<tr>
		<td>bytearray()</td>
		<td>float()</td>
		<td>list()</td>
		<td>raw_input()</td>
		<td>unichr()</td>
	</tr>
	<tr>
		<td>callable()</td>
		<td>format()</td>
		<td>locals()</td>
		<td>reduce()</td>
		<td>unicode()</td>
	</tr>
	<tr>
		<td>chr()</td>
		<td>frozenset()</td>
		<td>long()</td>
		<td>reload()</td>
		<td>vars()</td>
	</tr>
	<tr>
		<td>classmethod()</td>
		<td>getattr()</td>
		<td>map()</td>
		<td>repr()</td>
		<td>xrange()</td>
	</tr>
	<tr>
		<td>cmp()</td>
		<td>globals()</td>
		<td>max()</td>
		<td>reversed()</td>
		<td>zip()</td>
	</tr>
	<tr>
		<td>compile()</td>
		<td>hasattr()</td>
		<td>memoryview()</td>
		<td>round()</td>
		<td>_import_()</td>
	</tr>
	<tr>
		<td>complex()</td>
		<td>hash()</td>
		<td>min()</td>
		<td>set()</td>
		<td></td>
	</tr>
	<tr>
		<td>delattr()</td>
		<td>help()</td>
		<td>next()</td>
		<td>setattr()</td>
		<td></td>
	</tr>
	<tr>
		<td>dict()</td>
		<td>hex()</td>
		<td>object()</td>
		<td>slice()</td>
		<td></td>
	</tr>
	<tr>
		<td>dir()</td>
		<td>id()</td>
		<td>oct()</td>
		<td>sorted()</td>
		<td></td>
	</tr>
  </tbody>
</table>

另外，还有四个可选的内置函数：apply(),buffer(),coerce()和inter()。这四个可选内置函数都在Non-essential Build-in Functions部分中。

**abs(x)**<br>
  返回一个数的绝对值。参数可以为空或者长整型或者浮点型数字。如果参数是一个复数，则返回它的大小。

**all(iterable)**<br>
  如果iterable中的所有元素都为true(或者iterable为空)，返回 True,等价于：
```Python
def all(iterable):
	for element in iterable:
		if not element:
			return False
	return True
```

**any(iterable)**<br>
 只要iterable中任何一个元素为Ture就返回True，否则返回False,等价于：
```Python
def any(iterable):
	for element in iterable:
		if element:
			return True
		return False
```
**basestring()**<br>
 `str`和`unicode`的超类，不能被调用或实例化，但是可以判断一个对象是不是`str`或`unicode`类型。`isinstance(obj, basestring)`等价于`isinstance(obj,(str,unicode))`。
 
 **bin(x)**<br>
  将一个数字转换成一个二进制字符串。结果是一个有效的Python表达式。如果x不是一个Python int 对象，它必须定义一个_index_()方法，返回一个整数。
  
*class* **bool([x])**<br>
  返回一个布尔值，`True`或`False`。 如果*x*为false或者忽略，则返回**False**;否则返回 **True**。**bool**也是一个类，它是**int**的子类。**bool**不能再被继承。它只能实例化成**False**和**True**。
  
  *2.2.1版本的新特性*。<br>
  *在2.3中做了修改:* 如果不传参数，则返回**False**。
  
*class* **bytearray([source[,encoding[,errors]]])**<br>
  返回一个新的字节数组。**bytearray**类是一个可变的字节数组，它的范围是0~256。它具有可变序列类型的最常见的方法，以及大多数`str`类型的方法。<br>
  
  可选参数*source*可以使用以下几种方式初始化数组：<br>
  
  - 如果是 unicode,必须指定编码，然后使用**unicode.encode()**方法将unicode转换成字节。
  - 如果是 integer,该数组将以空字节大小来进行初始化。
  - 如果一个对象遵循 buffer接口，将使用这个对象的只读buffer来初始化数组。
  - 如果是一个iterable，它必须是范围在0~256的整数iterable，作为数组的初始化内容。

如果不传参数，则会创建一个长度为0的数组。

  *2.6版本中的新特性*
  
**callable(object)**<br>
  如果*ojbect*可以被调用，返回**True**，否则返回**False**。这个函数如果返回**True**，它也可能调用失败；但如果返回**False**,则*ojbect*永远不会调用成功。注意，类是可以被调用的；有_call_()方法的类实例也可以被调用。
  
**chr(i)**<br>
  返回一个ASCII码代表的字符。比如，`chr(97)` 返回字符 `a`。它跟 **ord**()相反。i的值必须在0~255之间；如果i的值超出255，则抛出**ValueError**异常。可以参见 **unichr**()。
  
**classmethod(function)**<br>
  指定一个方法为类方法。<br>
  类方法会将一个类隐式地作为第一个参数，就像实例方法会将实例作为自己的参数一样。将一个方法定义为类方法，如下：<br>
```Python
class C(object):
	@classmethod
	def f(cls,arg1,arg2,...):
	...
```
  `@classmethod`是一个函数装饰器，详细请参考 Funtion definitions 部分。<br>
  
  类方法既能被类调用（如`C.f()`）也能被实例调用（如`C().f()`）。如果一个类方法被子类调用，那么这个子类被隐式的传入类方法的第一个参数中。<br>
  
  Python的类方法不同于C++的类方法，也不同于Java的 static 方法。
  
**cmp(x,y)**<br>
  比较两个对象 x , y 的大小，输出一个整数。`x < y` 为负数，`x==y` 为 0，`x > y`为整数。

**compile(source,filename,mode[,flags[,dont_inherit]])**<br>
  将 source 编译成 code 或 AST 对象，Code 对象能够通过 **exec** 语句来执行或者 **eval()** 进行求值。<br>
  
  source: 既可以是 unicode 字符串，Latin-1 编码后的字符串也可以是 AST 对象。<br>
  filename: code文件名，如果不是从文件中读取则传递可用的值。<br>
  model: 编译code的种类，值可以为 ‘exec’,‘eval’,‘single’。<br>
  
```Python
	>>>code="print hello world"
	>>>cmp_code=compile(code,'','exec')
	>>>exec cmp_code
	hello world
```

class **complex([real[,imag]])**<br>
  返回一个值为 real + imag\*j 的复数，或者字符串或数转成一个复数。如果第一个参数为字符串，则不需要指定第二个参数。<br>
  real: int,long,float或字符串。<br>
  imag: int,long,float。
 
```Python
	>>>complex(1,2)
	(1+2j)
	>>>complex(1)
	(1+0j)
	>>>complex("1")
	(1+0j)
	>>>complex("1+2j")
	(1+2j)
```

**delattr(object,name)**<br>
  删除 `object` 对象中名为 `name` 的属性。跟 `setattr()` 相反。

```Python
	>>>class Person:
	...	def __init__(self,name,age):
	...		self.name=name
	...		self.age=age
	>>>wanglin=Person('Wanglin',28)
	>>>dir(wanglin)
	['__doc__','__init__','__module__','age','name']
	>>>delattr(wanglin,'name')
	>>>dir(wanglin)
	['__doc__','__init__','__module__','age']
```

class **dict(\*\*kwarg)**<br>
class **dict(mapping,\*\*kwarg)**<br>
class **dict(iterable,\*\*kwarg)**<br>
  创建一个字典。
  
```Python
	>>>d = dict()
	>>>print d
	{}
	>>>dd = dict(a=12,b=24,c=45)
	>>>print dd
	{'a':12,'b':24,'c':45}
	>>>ddd = map(lambda x,y:(x,y),range(1,4),list('abc'))
	>>>dddd = dict(ddd)
	>>>print dddd
	{1:'a',2:'b',3:'c'}
```
