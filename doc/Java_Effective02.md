### 扩展 equals 要遵守的约定
重写 equals 必须重写 hashCode
``` 
x.equals(null)=false
```
* 自反性 x.equals(x)=true
* 对称性 x.equals(y)=true，同样 y.equals(x)=true
* 传递性 x.equals(y)=true,x.equals(z)=true，则 y.equals(z)=true
* 一致性 x,y 未修改，则多次调用 x.equals(y) 结果不变