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

**abs**(x)<br>
	返回一个数字的绝对值。参数可以为空或者长整型或者浮点型数字。如果参数是一个复数，则返回它的大小。

**all**(iterable)<br>
	如果iterable中的所有元素都为true(或者iterable为空)，返回 True,等价于：
	
	```Python
	def all(iterable):
		for element in interable:
			if not element:
				return False
		return True
	```
