# OSMods
Repository of currently registered Obenseuer mods to be referenced externally.

# Registering your mod
In order to add a mod you have created onto the list, you must make a [Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) and modify mods.json to include your mod. The PR will be checked for proper JSON formatting and will then be pulled (hopefully automatically in the near future).

Structure of a mod:
```json
{
    "id": "owner.product" // This is a unique string identifier which will help identify this mod easily for dependency resolution and otherwise. Preferably, this should use Reverse Domain Name notation and be the same as your Harmony/BIE mod identifier.
    "displayName": "A Name The End-User Will See",
    "tagline": "Best Mod on the Market", // The user will see this below the mod's name.
    "description": "Some description. Will probably eventually be markdown but not used so leave an empty string or something." // Unused currently, I will see about doing this later because I have some ideas.
    "owner": "your-github-name", // Your Github name
    "repository": "repository-unique-identifier", // The repository name (the one used to clone it). 
    "releases": {
        // Dictionary of releases. The Keys represent game versions (below shown which are supported).
        // Values represent tags the manager should use to resolve the download link.
        // Tags should follow Semantic Versioning (x.y.z) at all times so the manager can properly compare them.
      "0.4.01": "1.0.0"
    },
    "dependencies": [ // An array of strings which represent unique identifiers for the mods so they can be loaded and downloaded first.
        "always-show-needs"
    ]
  }
```
