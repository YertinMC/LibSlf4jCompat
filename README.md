# LibSlf4jCompat

This plugin adds slf4j to Bukkit servers.

## Reason

Before [13w39a](https://minecraft.fandom.com/wiki/Java_Edition_13w39a)(not included, this is a snapshot of 1.7.2, note that 1.7 is only a pre-release of 1.7.2 after this snapshot), Minecraft uses `java.util.logging`(JUL or JDK14 Logging) as the logger of the game.

After [13w39a](https://minecraft.fandom.com/wiki/Java_Edition_13w39a)(included), Minecraft uses Log4j directly as the logger of the game.

After [1.17-pre1](https://minecraft.fandom.com/wiki/Java_Edition_1.17_Pre-release_1)(included), Minecraft added slf4j and its Log4j binding to instead direct using of Log4j.



slf4j is easy to use but not included in old versions, so you can use this plugin.

This plugin provided three jars:

- Only slf4j api
- API and JUL binding(for [13w38c](https://minecraft.fandom.com/wiki/Java_Edition_13w38c) and below, or 1.6.4 and below)
- API and Log4j binding(for [13w39a](https://minecraft.fandom.com/wiki/Java_Edition_13w39a) to [21w20a](https://minecraft.fandom.com/wiki/Java_Edition_21w20a), or 1.7 to 1.16.5)

## LICENSE

This project licensed under MIT license(same as slf4j).

For more information, see `LICENSE` file.

