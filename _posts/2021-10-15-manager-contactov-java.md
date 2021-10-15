---
layout: post
title: Список контактов на Java
subtitle: Список контактов на Java - Часть-1 (данные в коде)
tags: [java]
comments: true
---

## Система управления списком контактов

Чтобы мы могли дальше двигаться не просто рассматривая новое, а со смыслом и практикой, предлагаю 
начать разработку очень простого приложения, которое позволит нам задействовать описываемые технологии. 
Чтобы не придумывать что-то очень сложное, я буду делать простой список контактов, который будет 
иметь возможность делать основные операции (назовем их для дальнейших рассуждений «бизнес-действие»):

1. Просмотр списка контактов
2. Добавление контакта
3. Редактирование контакта
4. Удаление контакта
    
Также предлагаю делать свой вариант — например список машин в автосалоне, список заказов пиццы, 
список книг. Пусть он будет выглядеть практически так же, как мой, но это будет ваш собственный проект.

![Диаграмма классов ContactManager](https://github.com/evgenvandev/test/blob/gh-pages/assets/img/ContactProject.png){: .mx-auto.d-block :}

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg){: .mx-auto.d-block :}

Класс _**Contact**_

```java
package edu.javacourse.contact.entity;

/**
 *  Класс для хранения данных контакта
 */
public class Contact {
    // Идентификатор контакта
    private Long contactId;
    // Имя
    private String firstName;
    // Фамилия
    private String lastName;
    // Телефон
    private String phone;
    // email
    private String email;
    
    public Contact() {
    }
    
    public Contact(String firstName, String lastName, String phone, String email) {
        this.firstName = firstName;
        this.lastName = lastName;
        this.phone = phone;
        this.email = email;
    }
}
```
