# LibSlf4jCompat

![GitHub commit activity](https://img.shields.io/github/commit-activity/y/YertinMC/LibSlf4jCompat?style=flat-square)![GitHub contributors](https://img.shields.io/github/contributors/YertinMC/LibSlf4jCompat?style=flat-square)![GitHub release (latest by date)](https://img.shields.io/github/v/release/YertinMC/LibSlf4jCompat?style=flat-square)![GitHub forks](https://img.shields.io/github/forks/YertinMC/LibSlf4jCompat?style=flat-square)![GitHub Repo stars](https://img.shields.io/github/stars/YertinMC/LibSlf4jCompat?style=flat-square)![GitHub](https://img.shields.io/github/license/YertinMC/LibSlf4jCompat?style=flat-square)![GitHub issues](https://img.shields.io/github/issues/YertinMC/LibSlf4jCompat?style=flat-square)![GitHub pull requests](https://img.shields.io/github/issues-pr/YertinMC/LibSlf4jCompat?style=flat-square)![GitHub closed pull requests](https://img.shields.io/github/issues-pr-closed/YertinMC/LibSlf4jCompat?style=flat-square)![GitHub language count](https://img.shields.io/github/languages/count/YertinMC/LibSlf4jCompat?style=flat-square)![GitHub Workflow Status](https://img.shields.io/github/workflow/status/YertinMC/LibSlf4jCompat/Build?style=flat-square)

This plugin adds slf4j to Bukkit servers.

## Reason

Before [13w39a](https://minecraft.fandom.com/wiki/Java_Edition_13w39a)(not included, this is a snapshot of 1.7.2, note that 1.7 is only a pre-release of 1.7.2 after this snapshot), Minecraft uses `java.util.logging`(aka as JUL or JDK14 Logging) as the logger of the game.

After [13w39a](https://minecraft.fandom.com/wiki/Java_Edition_13w39a)(included), Minecraft uses Log4j directly as the logger of the game.

After [1.17-pre1](https://minecraft.fandom.com/wiki/Java_Edition_1.17_Pre-release_1)(included), Minecraft added slf4j and its Log4j binding to instead direct using of Log4j.



slf4j is easy to use but not included in old versions, so you can use this plugin.

This plugin provided three jars:

- Only slf4j api
- API and JUL binding(for [13w38c](https://minecraft.fandom.com/wiki/Java_Edition_13w38c) and below, or 1.6.4 and below)
- API and Log4j binding(for [13w39a](https://minecraft.fandom.com/wiki/Java_Edition_13w39a) to [21w20a](https://minecraft.fandom.com/wiki/Java_Edition_21w20a), or 1.7 to 1.16.5)

## Using

### For user

You can download the correct version(see [Reason](#Reason)) of release jar here and put it into `plugins` directory of the server.

### For developer

#### Step1. Bukkit

Add this to you `plugin.yml`:

```yaml
softdepend:
    - LibSlf4jCompat
```

#### Step2. SLF4J

Add slf4j dependency or use high version bukkit api.

**DO NOT add this plugin using maven, there are some error on maven publishing**

##### Gradle

```groovy
dependencies {
    implementation 'org.slf4j:slf4j-api:2.0.0-alpha5'
}
```

##### Maven

```xml
<dependency>
    <groupId>org.slf4j</groupId>
    <artifactId>slf4j-api</artifactId>
    <version>2.0.0-alpha5</version>
    <scope>compile</scope>
</dependency>
```

## LICENSE

This project licensed under MIT license(same as slf4j).

For more information, see `LICENSE` file.

