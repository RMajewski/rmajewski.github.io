---
title: Powermockito
tags: powermockito
---

Damit das Powermockito richtig arbeitet, muss zunächste der
Powermockito-TestRunner aufgerufen werden. Wenn eine statische Methode gemockt
werden soll, muss noch die Klasse angegeben werden.

{% highlight java %}
@RunWith(PowerMockRunner.class)
@PrepareForTest({StaticClass.class})
class TestClass {
  @Test
  public testTest() {
  }
}
{% endhighlight %}

Mit `@RunWith` wird die `PowerMockRunner`-Klasse als TestRunner festgelegt.
Damit kann Powermockito genutzt werden.

Mit `@PrepareForTest({})` Werden die Klassen festgelegt, die Powermockito
untersuchen bzw. mocken soll.
