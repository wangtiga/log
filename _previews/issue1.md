---
layout: page
title: issue1
---

## 关于 inline code 的 markdown 显示效果问题

none 和 c 类型的 inline code 都能正常显示浏览器窗口内，
超出部分会显示一个局部水平滚动条。
txt 类型就会显示到浏览器窗口外。

不只 txt 类型，我还试过  plain log 等都会显示到窗口外，
怀疑是所有未识别的类型都这样处理的。

那么，如何更改默的显示效果 ，让超长的内容都显示到水平滚条内呢？
或者，如何增加自定义的 inline code ？


```txt
txt
1. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
2. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
3. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
4. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
```



```
none
1. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
2. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
3. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
4. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
```

```c
c
1. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
2. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
3. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
4. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
```


它们生成的 html 代码如下所示

```html
<div class="page">
  
<pre><code class="language-txt">txt
1. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
2. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
3. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
4. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
</code></pre>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code>none
1. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
2. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
3. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
4. The article introduces the features of the Jekyll theme support.The article introduces the features of the Jekyll theme support.
</code></pre></div></div>

<hr>

  
</div>
```

---
