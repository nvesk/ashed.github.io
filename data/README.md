# Pliki serwerowe Ashed Launcher
# Pobrane z: https://data-v2.polyfrost.org (OneLauncher/Polyfrost)
# Zaadaptowane dla: Ashed Launcher (https://data-v2.nvesk.org)

## Struktura folderów

```
data/
└── ashedclient/                        ← to wgraj na serwer pod https://data-v2.nvesk.org/
    ├── versions/
    │   ├── metadata.json             ← lista wersji MC
    │   └── art/
    │       ├── Tricky_Trials.jpg
    │       ├── Copper_Age.jpg
    │       ├── Mounts_Mayhem.jpg
    │       ├── Tiny_Takeover.jpg
    │       └── Chaos_Cubed.jpg
    ├── bundles/
    │   ├── metadata.json             ← lista paczek modów
    │   └── generated/
    │       ├── hud-1.21.1-fabric.mrpack
    │       ├── performance-1.21.1-fabric.mrpack
    │       ├── pvp-1.21.1-fabric.mrpack
    │       ├── qol-1.21.1-fabric.mrpack
    │       ├── utility-1.21.1-fabric.mrpack
    │       └── ... (35 plików mrpack łącznie)
    └── CHANGE_LOG.md                 ← changelog (opcjonalny)
```

## Jak wgrać na serwer

### Opcja A — GitHub Pages (najprostsze, darmowe)
1. Stwórz nowe repo na GitHubie np. `ashed-data`
2. Wgraj cały folder `ashedclient/` do repo
3. Włącz GitHub Pages (Settings → Pages → Branch: main)
4. Zmień w kodzie `constants.rs`:
   ```
   META_URL_BASE = "https://twoj-nick.github.io/ashed-data"
   ```

### Opcja B — własny serwer nginx/caddy
Wgraj folder `ashedclient/` na serwer i ustaw CORS:
```nginx
add_header Access-Control-Allow-Origin *;
```

### Opcja C — Cloudflare Pages / Netlify / Vercel
Wgraj zawartość `ashedclient/` jako projekt statyczny.

## Co zawierają paczki (.mrpack)

| Nazwa | Opis |
|-------|------|
| `hud-*` | HUD mody (minimap, armorStatus, itd.) |
| `performance-*` | Optymalizacja (Sodium, Lithium, itd.) |
| `pvp-*` | PvP mody |
| `qol-*` | Quality of Life |
| `skyblock-*` | SkyBlock mody |
| `utility-*` | Utility mody |

## Wersje Minecraft w manifest

- **1.21.1** — Tricky Trials (Fabric)
- **1.21.10** — The Copper Age (Fabric)
- **1.21.11** — Mounts of Mayhem (Fabric)
- **26.1** — Tiny Takeover (Fabric)
- **26.1.2** — (Fabric)
- **26.2** — Chaos Cubed (Fabric)
