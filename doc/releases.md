
```shell script
vim ~/.m2/settings.xml

mvn clean install -Dmaven.test.skip=true
mvn clean deploy -P release-sign-artifacts -Dmaven.test.skip=true
```

```xml
<?xml version="1.0" encoding="UTF-8"?>

<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
          xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 http://maven.apache.org/xsd/settings-1.0.0.xsd">
  <pluginGroups>
  </pluginGroups>

  <servers>
    <server>
      <id>ossrh</id>
      <username>HejinYo</username>
      <password>************</password>
    </server>
  </servers>

  <mirrors>
     <mirror>
        <id>nexus-aliyun</id>
        <mirrorOf>central</mirrorOf>
        <name>Nexus aliyun</name>
        <url>http://maven.aliyun.com/nexus/content/groups/public</url>
    </mirror>
  </mirrors>
</settings>

```

https://s01.oss.sonatype.org/#view-repositories;releases~browsestorage

https://central.sonatype.org/publish/publish-maven/

