# see-versions

Manifeste public des versions des ressources Unsee.

Ce depot ne contient **aucun code** : uniquement le fichier `versions.json`, lu automatiquement par `see_lib` pour signaler qu'une mise a jour est disponible.

## Format

```json
{
    "updated_at": "2026-08-16",
    "store": {
        "name": "Unsee Store",
        "url": "https://portal.cfx.re/assets/granted-assets"
    },
    "packages": {
        "see_admin": {
            "label": "Unsee Admin",
            "version": "1.0.2",
            "released_at": "2026-08-16",
            "changelog": ["fix: corrige le noclip en vehicule"]
        }
    }
}
```

| Champ | Role |
|---|---|
| `store.name` / `store.url` | Credits et lien affiches dans la console quand une mise a jour existe |
| `packages.<ressource>.version` | Derniere version publiee, comparee a celle du `fxmanifest.lua` installe |
| `packages.<ressource>.changelog` | Lignes affichees a l'utilisateur (uniquement les changements qui le concernent) |

Les versions suivent le format strict `X.Y.Z`.

## Mise a jour

Le fichier est genere par la commande `bun see release <ressource> <version>` du projet Unsee. Toute edition manuelle doit conserver le meme format.
