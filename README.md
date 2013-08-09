MavenRepo
=

This git repository contains a maven repository for artifacts of my projects. To deploy artifacts, clone this repository next to the project you want to deploy (in other words, the path `${basedir}/../MavenRepo` should points from the project's POM to this repository), and then do a `mvn deploy`.

You won't usually need to clone this repository. Maven projects referencing some of mine should use some code like this in their POM to have access to the artifacts:

    TODO verify this code snippet is correct

```
 <repositories>
  <repository>
   <id>SillyFreak-releases</id>
   <url>https://raw.github.com/SillyFreak/MavenRepo/master/releases/</url>
   <releases>
    <enabled>true</enabled>
   </releases>
   <snapshots>
    <enabled>false</enabled>
   </snapshots>
  </repository>
  <repository>
   <id>SillyFreak-snapshots</id>
   <url>https://raw.github.com/SillyFreak/MavenRepo/master/snapshots/</url>
   <releases>
    <enabled>false</enabled>
   </releases>
   <snapshots>
    <enabled>true</enabled>
   </snapshots>
  </repository>
 </repositories>
```

