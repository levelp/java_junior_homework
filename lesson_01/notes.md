Непрерывная интеграция
---

**Как настроить travis?**
1. Зайти на сайт https://travis-ci.org/
1. Войти с помощью логина github, дать авторизацию travis.
1. В списке репозиторие включить непрерывную интеграцию у нужного репозитория.
1. Добавить в ваш проект в корень файл с названием **.travis.yml**, содержащий следующие строчки:
```YML
language: java
jdk:
  - oraclejdk8
```


Maven
---

Перед создание Maven-проекта прочитайте статьи о стандартной архитектуре каталогов проекта Maven и что там находится.

**Простейший проект на Maven**
```XML
?xml version="1.0" encoding="UTF-8"?>
<project xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xmlns="http://maven.apache.org/POM/4.0.0"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <!-- POM = Project Object Model -->
    <groupId>ru.levelp</groupId>
    <artifactId>ProjectExample</artifactId>
    <version>1.0-SNAPSHOT</version>

    <properties>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
        <project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>
        <!-- Версия Java которой мы будем компилировать -->
        <java.version>1.8</java.version>
    </properties>

    <dependencies>
    </dependencies>

    <build>
        <pluginManagement>
            <plugins>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-compiler-plugin</artifactId>
                    <version>3.1</version>
                    <configuration>
                        <!-- Версия Java для исходников -->
                        <source>${java.version}</source>
                        <!-- Версия Java для байт-кода -->
                        <target>${java.version}</target>
                    </configuration>
                </plugin>
            </plugins>
        </pluginManagement>
    </build>
</project>

```


**Как добавить в проект junit?**
Необходимо добавить в конфигурацию в **dependencies** тег следующий код:
```XML
<dependency>
    <groupId>junit</groupId>
    <artifactId>junit</artifactId>
    <version>4.11</version>
    <scope>test</scope>
</dependency>
```
