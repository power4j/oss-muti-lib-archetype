[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.power4j.archetype/oss-lib-multi/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.power4j.archetype/oss-lib-multi)

## usage

New project GAV:  `com.example:demo:1.0.0-SNAPSHOT`

```shell
mvn archetype:generate \
       -DgroupId=com.example \
       -DartifactId=demo \
       -Dversion=1.0.0-SNAPSHOT \
       -Dpackage=com.example \
       -DarchetypeGroupId=com.power4j.archetype \
       -DarchetypeArtifactId=oss-lib-multi \
       -DarchetypeVersion=1.0.0
```

you will get
```
│
├─ .springjavaformatconfig
├─ HELP.md
├─ LICENSE
├─ mvnw
├─ mvnw.cmd
├─ ossrh-settings.xml
├─ pom.xml
├─ README.md
│
├─.github            # GitHub CI
├─demo-build         # Internal module for build management
├─demo-core          # The default library,For complex projects, there may be multiple similar directories 
└─demo-dependencies  # BOM used by library users
```

you can use  `-DarchetypeCatalog=local` for local test

required properties

- `githubPath`: used to generate urls, for example your project url is `https://github.com/your-name/hello-world`, the value should be `your-name/hello-world` 
- `developerName`/`developerEmail`: your name and email
