# Folia Builds

Provides pre-compiled builds of the [Folia](https://github.com/PaperMC/Folia) server so you don't have to build it yourself.

## Why?

> [!WARNING]
> 
> The provided pre-compiled builds are unofficial as I am not affiliated with the PaperMC team in any way.
> So if you encounter any issues, you should ask PaperMC for [support](https://github.com/PaperMC/Folia/issues), not me.
> 
> Also, you should already know that Folia breaks many vanilla commands, APIs, and plugins and is still in development.
> That's why you should use Folia on your own risk. I have warned you.

The PaperMC team decided not to provide official builds for Folia, as it is still in development and only suitable for
a very few amount of servers (major SMP, skyblock, etc. servers).
So, in order to use Folia, you need to build it yourself. However, this takes time (especially if you're a Windows user).
That's why I decided to share ready-made unofficial builds of Folia for myself and for you to use.

## How to Build (by yourself)

> [!NOTE]
> 
> I would recommend you to prefer using Linux over Windows to build Folia because it will take much more time to build on Windows than on Linux.
> For me, it took over an hour to build Folia on Windows. The most time-consuming part for me was applying patches: it took me about ~45-50 minutes.

> [!IMPORTANT]
> 
> **Requirements:**
> - Git
> - Java 17 LTS
> - Internet connection _(obviously)_

### Instructions

1. Clone the official repository:
```bash
git clone https://github.com/PaperMC/Folia.git
```

2. Checkout branch (if you want to use a specific Minecraft version instead of latest; otherwise, you can simply skip this step):
   - For Minecraft 1.21.4:
   ```bash
   git checkout ver/1.21.4
   ```
   - For Minecraft 1.21.3:
   ```bash
   git checkout dev/1.21.3
   ```
   - For Minecraft 1.21.1:
   ```bash
   git checkout dev/1.21.1
   ```
   - For Minecraft 1.20.4:
   ```bash
   git checkout ver/1.20.4
   ```
   - For Minecraft 1.19.4:
   ```bash
   git checkout ver/1.19.4
   ```

3. Apply patches:
   - On Unix/Linux (or with Bash):
   ```bash
   ./gradlew applyPatches
   ```
   - On Windows (with cmd):
   ```batch
   gradlew applyPatches
   ```

4. Build:
   - Create a reobfuscated paperclip jar file:
     - On Unix/Linux (or with Bash):
     ```bash
     ./gradlew createReobfPaperclipJar
     ```
     - On Windows (with cmd):
     ```batch
     gradlew createReobfPaperclipJar
     ```
   - Create a reobfuscated bundler jar file:
     - On Unix/Linux (or with Bash):
     ```bash
     ./gradlew createReobfBundlerJar
     ```
     - On Windows (with cmd):
     ```batch
     gradlew createReobfBundlerJar
     ```
   - Create a Mojang-mapped paperclip jar file:
     - On Unix/Linux (or with Bash):
     ```bash
     ./gradlew createMojmapPaperclipJar
     ```
     - Windows (with cmd):
     ```batch
     gradlew createMojmapPaperclipJar
     ```
   - Create a Mojang-mapped bundler jar file:
     - On Unix/Linux (or with Bash):
     ```bash
     ./gradlew createMojmapBundlerJar
     ```
     - On Windows (with cmd):
     ```batch
     gradlew createMojmapBundlerJar
     ```

## Acknowledgements
- [Slackadays/FoliaToGo](https://github.com/Slackadays/FoliaToGo) - 🥡🤖 Nightly builds of the Folia server jar, ready-to-use, right here
