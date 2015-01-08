---
layout: post
title:  "Go in Chinese"
---

About a million years ago, I wrote a blog post titled ["Ruby in Chinese".

After spending the past few months learning Go, I had a similar question;

> Is it possible to write Go in Chinese?

You'd think it might just work

{% highlight go %}
package main

import "fmt"

func main() {
  fmt.Println("你好，世界")
}
{% endhighlight %}

And it sure does work.

But we can do better, we can assign instance variables with chinese names.

{% highlight go %}
句子 := "你好，世界"
fmt.Println(句子)
{% endhighlight %}

or write functions with chinese names;

{% highlight go %}
func main() {
  說話("你好，世界")
}

func 說話(句子 string) {
  fmt.Println(句子)
}
{% endhighlight %}

And if we're feeling cheeky we can alias types to chinese names.

{% highlight go %}
type 字符串 string

func 說話(句子 字符串) {
  fmt.Println(句子)
}
{% endhighlight %}

In fact we can write

{% highlight go %}
package 動物

interface 動物 {
  叫() 字符串
}

type 狗 struct {
  名字 字符串
}

func (g *狗) 叫() 字符串 {
  return "汪汪"
}
{% endhighlight %}
