Maven
---

**Как добавить в проект Hibernate?**
Необходимо добавить в конфигурацию в **dependencies** тег следующий код:
```XML
<dependency>
    <groupId>org.hibernate</groupId>
    <artifactId>hibernate-core</artifactId>
    <version>RELEASE</version>
</dependency>
<dependency>
    <groupId>org.hibernate</groupId>
    <artifactId>hibernate-entitymanager</artifactId>
    <version>RELEASE</version>
</dependency>
```


Для других баз смотрите [пример](https://github.com/levelp/Hibernate/blob/master/pom.xml).

