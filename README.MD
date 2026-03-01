# Dumpster Fire Plugins

This repository aggregates every one of my Dalamud plugin projects so I can hand out a **single** repo URL when sharing builds.

## Included plugins

1. **Chocobo Colourized** – calculate optimal fruit feeding plans for chocobo recolours.
2. **Fren Rider** – multibox follow + automation companion for two or more characters.

## Dalamud repo URL

```
https://raw.githubusercontent.com/McVaxius/TheDumpsterFire/main/repo.json
```

Paste the URL above into Dalamud → Settings → Experimental → Custom Plugin Repositories to access every plugin at once.

## Keeping the repo up to date

- Each plugin repo (ChocoboColourized, FrenRider) still contains its own `repo.json` and release workflow.
- The root-level `bump-version.py` script now updates **all** repo manifests (individual + master) so versions stay in sync.
- After bumping + tagging a plugin release, commit the regenerated manifests and push. The master repo will always track the latest published versions.

Please enjoy the growing dumpster fire. 🔥