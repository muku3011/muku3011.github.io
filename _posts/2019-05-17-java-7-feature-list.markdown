---
layout: post
title:  "Java 7 feature list!"
date:   2019-05-17 20:53:00
categories: Java
---

### Try-with-resources statement

{% highlight ruby %}
BufferedReader br = new BufferedReader(new FileReader(path));
 try {
    return br.readLine();
 } finally {
    br.close();
 }
{% endhighlight %}

{% highlight ruby %}
try (BufferedReader br = new BufferedReader(new FileReader(path)) {
   return br.readLine();
}
#=> You can declare more than one resource to close:
try (
   InputStream in = new FileInputStream(src);
   OutputStream out = new FileOutputStream(dest))
{
 // code
}
{% endhighlight %}