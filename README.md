# mongeez-maven-plugin
Maven plugin for MongoDB migrations (uses [Mongeez](https://github.com/mongeez/mongeez))

#### Current version: 0.9.2

### Usage

1. Add build plugin dependency to your POM

    ```xml
    <build>
        <plugins>
            <plugin>
                <groupId>pl.coderion.mongodb</groupId>
                <artifactId>mongeez-maven-plugin</artifactId>
                <version>0.9.3</version>
                <configuration>
                    <dbName>test</dbName>
                    <changeLogFile>src/main/mongeez/mongeez.xml</changeLogFile>
                </configuration>
            </plugin>
        </plugins>
    </build>
    ```

2. Run maven goal:

    ```
    mvn mongeez:update
    ```


### Configuration

* ##### optional db authentication

    ```xml
    <configuration>
        <dbName>test</dbName>
        <dbAuth>true</dbAuth>
        <username>foo</username>
        <password>bar</password>
        <changeLogFile>src/main/mongeez/mongeez.xml</changeLogFile>
    </configuration>
    ```

Example usage:

    ```xml
    <build>
        <plugins>
            <plugin>
                <groupId>pl.coderion.mongodb</groupId>
                <artifactId>mongeez-maven-plugin</artifactId>
                <version>0.9.3</version>
                <configuration>
                    <dbName>test</dbName>
                    <changeLogFile>src/main/mongeez/mongeez.xml</changeLogFile>
                </configuration>
            </plugin>
        </plugins>
    </build>
    ```

* ##### changeLogFile

Create _mongeez.xml_ with all change logs. See [how to use mongeez](https://github.com/mongeez/mongeez/wiki/How-to-use-mongeez).

### Travis Continuous Integration Build Status

[![Build Status](https://travis-ci.org/coderion/mongeez-maven-plugin.svg?branch=master)](https://travis-ci.org/coderion/mongeez-maven-plugin)

### License
Licensed under the Apache License, Version 2.0: http://www.apache.org/licenses/LICENSE-2.0