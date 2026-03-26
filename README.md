# Cobbleverse Neo

An unofficial NeoForge port of the Cobbleverse Fabric modpack for Minecraft 1.21.1.

## Building

The `port-cobbleverse.ps1` script (available in [Releases](https://github.com/UmushiUmushi/Cobbleverse-Neo/releases)) converts the original Fabric pack into a CurseForge-importable NeoForge zip.

### Requirements

- **COBBLEVERSE - Pokemon Adventure [Cobblemon]** installed via CurseForge
- Windows with PowerShell 5.1+
- Internet connection (downloads 4 files from GitHub/Modrinth)

### Steps

1. Install **COBBLEVERSE - Pokemon Adventure [Cobblemon]** from CurseForge.

2. Open PowerShell and run:
   ```powershell
   powershell -ExecutionPolicy Bypass -File "path\to\port-cobbleverse.ps1"
   ```
   The script auto-detects the Fabric instance if it's in the standard CurseForge Instances directory alongside the script.

3. Import the output zip into CurseForge:
   **Create Custom Profile** > **Import** (icon at top right) > select the zip.

To specify paths explicitly:
```powershell
.\port-cobbleverse.ps1 -FabricPath "C:\path\to\COBBLEVERSE - Pokemon Adventure [Cobblemon]" -OutputPath "C:\tmp\Cobbleverse.Neo.zip"
```

### What the script does

1. Copies configs, resource packs, shader packs, datapacks from the Fabric instance
2. Copies Fabric-only mods that run through Sinytra Connector
3. Downloads mods not available via CurseForge (BetterRecipeBook, LenientDeath, Cobbreeding, Cobblemon Additions)
4. Patches Debugify (removes incompatible mixins for NeoForge)
5. Patches CCCC resource pack (fixes bedrock poser format for NeoForge)
6. Updates configs (FancyMenu class names, resource pack load order, Connector/Debugify)
7. Generates a CurseForge manifest with all mod project/file IDs
8. Packages everything into a CurseForge-importable zip

## About

Cobbleverse is a Cobblemon-based modpack originally built on Fabric. Cobbleverse Neo is an unofficial from-scratch port to NeoForge using Sinytra Connector for Fabric mod compatibility.

See `PORT_DOCUMENTATION.md` inside the modpack for full details on the port process, mod replacements, and known issues.

## License

See [LICENSE](LICENSE) for details.

## Disclaimer

The original COBBLEVERSE modpack is created by and belongs to [LUMYVERSE](https://www.curseforge.com/members/lumyverse). This is an unofficial port and is not affiliated with or endorsed by LUMYVERSE.
