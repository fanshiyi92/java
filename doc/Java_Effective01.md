
### Java 静态工厂方法与构造器

#### 优势:
* 静态工厂方法相较于构造器的第一大优势在于它们有名称
* 静态工厂方法相较于构造器的第二大优势在于不必在每次调用的时候都重新创建对象
* 静态工厂方法相较于构造器的第三大优势在于可以返回原始类型的任何子类型的对象（根据『里氏替换』原则，即子类能替换父类）
* 代码相对简洁

```
public class ConstructerFactoryTest {
	private static ConstructerFactoryTest cft1;
	private ConstructerFactoryTest(){}

    public static ConstructerFactoryTest getCFT() {
    if (cft1== null) {
        cft1= new ConstructerFactoryTest();
    }
    // 或者 return ConstructerFactoryTest 的扩展类
    return cft1;
    }
}

```

#### 劣势:
* 静态工厂的主要缺点在于类必须含有公有或者受保护的构造器，负责无法被子类化
* 静态工厂方法目前提供的帮助文档很少