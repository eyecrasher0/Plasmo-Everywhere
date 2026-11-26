# Plasmo Everywhere

A client-side addon for Plasmo Voice that lets nearby players talk on Minecraft servers without a voice chat plugin. Nothing needs to be installed on the Minecraft server.

[Download](https://github.com/eyecrasher0/Plasmo-Everywhere/releases)

## Requirements

Choose the JAR for your Minecraft version and loader: **Fabric, Forge or NeoForge**. Install the matching **Plasmo Voice** client. Fabric also requires Fabric API. Available combinations are listed with the release files.

Use the Java runtime required by your Minecraft version. Builds for Minecraft releases through 1.20.4 require Java 17 or later.

## Installation and use

Put the Plasmo Everywhere JAR and its dependencies in your `mods` folder. Everyone you want to talk to needs the addon and Plasmo Voice installed.

Join the same Minecraft server. Voice connects automatically, including nearby player discovery across different server addresses when both players use compatible builds. Use the normal Plasmo Voice controls for your microphone, push-to-talk and volume. Open **Esc → Everywhere** to check the connection or reconnect.

The addon automatically selects a low-latency relay. Players connected through different project relays can still talk together. It tries to connect players directly and uses a relay when a direct connection is unavailable. Servers with their own Plasmo Voice setup take priority automatically.

## Build

Each `<loader>/<minecraft-version>/` folder is a standalone Gradle project. Use its Gradle wrapper and a compatible JDK. For example, with Java 25:

```sh
cd fabric/26.3
./gradlew build
```

The client JAR is written to that folder’s `build/libs/`. Choose the JAR without `sources`, `thin` or `dev` in its name.

## License

[GPL-3.0-only](LICENSE).
