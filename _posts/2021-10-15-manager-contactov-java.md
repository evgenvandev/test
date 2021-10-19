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

![Диаграмма классов](https://raw.githubusercontent.com/evgenvandev/test/gh-pages/assets/img/ContactProject.png "Диаграмма классов")

Класс _**Contact**_

Этот класс не должен вызывать каких-то больших вопросов. Там перечислены нужные поля и для них сделаны сетеры и гетеры. Может вызывать 
сомнение набор конструкторов - я сделал для всех полей (в случае редактирования) и все поля кроме ИД (id) - для случая добавления. Мне 
показалось, что так будет удобно. Переопределение метода _**toString**_ сделано для удобства вывода информации о контакте.

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
    
    public Contact(Long contactId, String firstName, String lastName, String phone, 
                    String email) {
        this.contactId = contactId;
        this.firstName = firstName;
        this.lastName = lastName;
        this.phone = phone;
        this.email = email;
    }
    
    public Long getContactId() {
        return contactId;
    }
    
    public void setContactId(Long contactId) {
        this.contactId = contactId;
    }
    
    public String getFirstName() {
        return firstName;
    }
    
    public void setFirstName(String firstName) {
        this.firstName = firstName;
    }
    
    public String getLastName() {
        return lastName;
    }
    
    public void setLastName(String lastName) {
        this.lastName = lastName;
    }
    
    public String getPhone() {
        return phone;
    }
    
    public void setPhone(String phone) {
        this.phone = phone;
    }
    
    public String getEmail() {
        return email;
    }
    
    public void setEmail(String email) {
        this.email = email;
    }
    
    @Override
    public String toString() {
        return "Contact{" + "contactId=" + contactId + ", firstName=" + firstName + 
                ", lastName=" + lastName + ", phone=" + phone + ", email=" + email + "}";
    }
}
```
