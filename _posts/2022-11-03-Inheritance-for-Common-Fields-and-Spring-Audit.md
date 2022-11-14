---
layout: post
title: "Inheritance for Common Fields and Spring Audit"
author: canis
categories: 
- spring
- springframework
image: assets/images/database-audit-columns-01.jpeg
---

In this article, we are going to focus on common fields and how it can affect our application if we do not plan ahead of time.  
  
## Introduction

The Common fields are fields that are similar and present in two or more classes in Java.

Declaring common fields for each class in a scalable project could be cumbersome as it makes you repeat yourself and could make lengthy codes.  
But how about dealing with timestamp fields?  Is there another way we could implement it seamlessly? Let’s find out. 

## DRY Principle and Inheritance

The DRY principle is a technique that most developers employ, particularly in Object Oriented Programming. DRY is an acronym that stands for Do Not Repeat Yourself. It simply means you should not write the same code over and over again.

You are doing the same thing twice if your application has similar fields or codes spread across numerous classes. As a result, you are not following the principle. It will be challenging to manage and maintain, and if there are any changes, you will need to update it everywhere you write it, taking time away from everyone.

Breaking down your code and logic into smaller yet reusable components can help to prevent this worst-case situation. It is better to have less and simpler code because it will take less time and effort to maintain, will be easier to update, and will be less likely to include bugs.

A way of applying the DRY principle is to make use of inheritance. Inheritance means that a class can inherit all the properties from another class. With that being said, we remove code duplication and we are not repeating ourselves, thus it allows us to reuse the code.

## Spring Audit

Now that we are aware of how to reuse common fields rather than rewriting them for every class. With regards to timestamp fields, we are moving forward together with Spring. Introducing Spring Audit, every change we make to our persistent data is tracked and logged by this feature, which also tracks and logs all insert, update, and delete activities. Additionally, it is necessary for tracking user activities.

The first two examples use Spring Audit but have the same timestamp fields which cause lengthy code and not applying reusability.
 
According to the [spring documentation](https://docs.spring.io/spring-data/jpa/docs/current/api/org/springframework/data/jpa/domain/support/AuditingEntityListener.html#:~:text=Class%20AuditingEntityListener&text=Configures%20the%20AuditingHandler%20to%20be,on%20the%20domain%20types%20touched.&text=Sets%20modification%20and%20creation%20date,implements%20Auditable%20on%20persist%20events.), the AuditingEntityListener is a JPA entity listener for auditing information on persisting and modifying entities.

```
@Entity
@EntityListeners(AuditingEntityListener.class)
public class Employees{

  @Id
  @GeneratedValue(strategy = GenerationType.IDENTITY)
  private int id;

  private String lastName;

  private String firstName;

  private String email;

  private String password; 

  @LastModifiedBy
  @Column(columnDefinition = "bigint default 1")
  private Long updatedBy;

  @LastModifiedDate
  private LocalDateTime updatedAt;

  @CreatedDate
  private LocalDateTime createdAt;

  private LocalDateTime deletedAt;  

  // getters and setters
}

  
@Entity
@EntityListeners(AuditingEntityListener.class)
public class Holidays {

  @Id
  @GeneratedValue(strategy = GenerationType.IDENTITY)
  private int id;

  private String holidayName;

  private LocalDate holidayDate;

  @LastModifiedBy
  @Column(columnDefinition = "bigint default 1")

  private Long updatedBy;

  @LastModifiedDate
  private LocalDateTime updatedAt;

  @CreatedDate
  private LocalDateTime createdAt;

  private LocalDateTime deletedAt;

  // getters and setters
}
```

  
The following examples use inheritance. Notice that there is reusability of code and it is smaller and cleaner code to look at.

  
```
@MappedSuperclass
@EntityListeners(AuditingEntityListener.class)
public abstract class Auditable {

  @LastModifiedBy
  @Column(columnDefinition = "bigint default 1")
  private Long updatedBy;

  @LastModifiedDate
  private LocalDateTime updatedAt;

  @CreatedDate
  private LocalDateTime createdAt;

  private LocalDateTime deletedAt;
  // getters and setters
}  

@Entity
public class Employees extends Auditable{

  @Id
  @GeneratedValue(strategy = GenerationType.IDENTITY)
  private int id;

  private String lastName;

  private String firstName;

  private String email;

  private String password;

  // getters and setters
}


@Entity
public class Holidays {

  @Id
  @GeneratedValue(strategy = GenerationType.IDENTITY)
  private int id;

  private String holidayName;

  private LocalDate holidayDate;

  // getters and setters
}
```

  

## Summary

This article focused on what are common fields and how to reuse them in order to apply DRY principle and also knowing Spring Audit which can give a big help for tracking and logging user activities in the database. In the example given, we had noticed the lengthy code and repetitive audit fields in the Employees and Holidays class respectively. If there is a change in the database implementation, suppose we are removing some audit field for all classes, which means we will waste a lot of time rewriting again for each class. So for that not to happen we then try to remove the repetition and encourage reusability by applying the DRY principle and inheritance.
