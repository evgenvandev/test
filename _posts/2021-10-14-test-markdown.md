---
layout: post
title: Пример сообщения в блоге
subtitle: У каждого сообщения также есть подзаголовок
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [test]
comments: true
---

Это демонстрационный пост, чтобы показать вам, как писать сообщения в блоге с markdown.  Я настоятельно рекомендую вам [потратить 5 минут на то, чтобы научиться писать в markdown](https://markdowntutorial.com/) - это научит вас преобразовывать обычный текст в полужирный/курсив/заголовки/таблицы и т.д.

**Вот некоторый жирный текст**

## Вот второстепенный заголовок

Вот бесполезная таблица:

| Число | Следующее число | Предыдущее число |
| :------ |:--- | :--- |
| Пять | Шесть | Четыре |
| Десять | Одиннадцать | Девять |
| Семь | Восемь | Шесть |
| Два | Три | Один |


Как насчет вкусного блинчика?

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg)

Его также можно центрировать!

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg){: .mx-auto.d-block :}

Вот фрагмент кода:

~~~
var foo = function(x) {
  return(x + 5);
}
foo(3)
~~~

А вот тот же код с подсветкой синтаксиса:

```javascript
var foo = function(x) {
  return(x + 5);
}
foo(3)
```

И снова тот же код, но с номерами строк:

{% highlight javascript linenos %}
var foo = function(x) {
  return(x + 5);
}
foo(3)
{% endhighlight %}

## Коробки
Вы можете добавить поля уведомлений, предупреждений и ошибок следующим образом:

### Уведомление

{: .box-note}
**Примечание:** Это окно с уведомлением.

### Предупреждение

{: .box-warning}
**Предупреждение:** This is a warning box.

### Ошибка

{: .box-error}
**Ошибка:** Это окно с ошибкой.