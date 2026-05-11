# plg_tags_og

Plugin pro OpenGraph a Twitter Card metadata podle tagů a obsahu.

## Metadata

| Pole | Hodnota |
| :--- | :--- |
| Typ | `plugin` |
| Verze | `0.1.1` |
| Vendor | `klucon` |
| Extension ID | `klucon/plg_tags_og` |
| Kategorie | `seo` |
| Licence | MIT |
| Core minimum | `0.1.0` |
| Python | `>=3.12` |
| Entry point | `src.plugins.plg_tags_og` |
| Admin URL | `-` |

## Účel

Tagy - OpenGraph je marketplace rozšíření pro KLUCON CMS. Balíček je určený pro instalaci přes `/admin/marketplace` a musí projít validací manifestu, checksumu a podpisu.

## Struktura

```text
src/**/plg_tags_og/
├── manifest.json
├── __init__.py
├── i18n/
└── ...
```

Manifest používá schema `1.0`, deklaruje typ `plugin`, kompatibilitu s core, i18n doménu `plg_tags_og` a bezpečnostní capabilities. Implementace obsahuje hook handlery.

## Balíčkování

Release ZIP se staví z `src/**/plg_tags_og/manifest.json` pomocí GitHub Actions workflow `.github/workflows/release-package.yml`. Do balíčku nepatří cache, `.git`, lokální ZIP artefakty ani dočasné soubory.

## Instalace

1. Publikuj ZIP a metadata do marketplace serveru.
2. V CMS otevři `/admin/marketplace`.
3. Vyber `plg_tags_og` a instaluj verzi `0.1.1`.
4. Po instalaci ověř záznam v příslušné tabulce `installed_*`.

## Poznámky k verzi

Aktualizace dokumentace a rebuild balíčku pro GitHub distribuci.
