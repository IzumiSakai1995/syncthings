**3.7 版本以后标准库提供**

filed  提供默认值
参数
1. default: 如果提供，这将是该字段的默认值。这是必须的，因为filed() 调用本身会替换一般的默认值
2. defualt_factory：如果提供，它必须是一个零参数的可调用对象，当该字段需要一个默认值时，它将被调用

```python
@dataclass
class C:
	mylist:list[int] = filed(default_factory=list)
```

#### 类变量

