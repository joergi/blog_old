---
title: "Exclude one element from Lombok model-wide setter and getter"
description: "Using Lombok @Setter and @Getter for all elements, but skip it for one element"
categories: [java, lombok]
tags: [lombok, java]
date: 2020-03-27
---

Lets say you have a model like this:

```java
 
@Getter
@Setter
public class User {

    @Id
    private String id;

    private String username;

    private String email;

    private String password;
}
```

```setId(String id)``` makes no sense.    
Normally the id is set by the DB, so it makes no sense to set it.

So you can use ```  @Setter(AccessLevel.NONE)```   (or   ```@Getter(AccessLevel.NONE```)) to exclude it from the Lombok setters (or getters)

```java

@Getter
@Setter
public class User {

    @Id
    @Setter(AccessLevel.NONE)
    private String id;

    private String username;

    private String email;

    private String password;
}
```
