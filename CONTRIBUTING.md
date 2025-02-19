# Contributing

## Develop

#### 1. Fork it

#### 2. Build the project

```shell
# java 8 required
`export JAVA_HOME=/path/to/java8/home`

mvn clean compile test
```

#### 3. Make a change

fix a bug, add a feature, update the doc, etc

#### 4. Run the Tests

```shell
mvn test
```

#### 5. Create a PR

## Misc

#### Add yourself as a contributor

After your PR has been merged, add yourself as a contributor.

To do so, add a comment like the following on your PR:

@all-contributors please add @your-username for code and test!

_Replace code with doc or test or infra or some combination depending on your contribution._

#### Package

Contributors are not responsible for pushing packages to mavencentral and jcenter. Contributors are responsible for validating that the package step succeeds.

```shell
mvn clean package dokka:javadocJar
```

### Publish to Github Packages

Add `distributionManagement` to `pom.xml`

```xml
  <distributionManagement>
    <repository>
      <id>github</id>
      <name>Carmine M DiMascio</name>
      <url>https://maven.pkg.github.com/cdimascio/dotenv-kotlin</url>
    </repository>
  </distributionManagement>
```

```shell
# deploy to github packages
mvn deploy -Dregistry=https://maven.pkg.github.com/cdimascio -Dtoken=XXXX
```
https://docs.github.com/en/packages/using-github-packages-with-your-projects-ecosystem/configuring-apache-maven-for-use-with-github-packages
