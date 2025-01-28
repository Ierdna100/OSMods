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
    "latestVersionTag": "tag-release", // The Tag the manager should look for when resolving your download link. 
    "owner": "your-github-name", // Your Github name
    "repository": "repository-unique-identifier", // The repository name (the one used to clone it). 
    "compatibilityVersionTags": { // Dictionary used to support previous versions of the game. The key corresponds to a certain version of the game we can rollback to (below are examples, none are currently supported) while the value is the tag the manager will look for to resolve the download link.
      "0.3.22": "0.0.1",
      "0.3.29": "0.0.2",
      "0.3.33": "0.0.3",
      "0.0.38": "0.0.4"
    },
    "dependencies": [ // An array of strings which represent unique identifiers for the mods so they can be loaded and downloaded first.
        "always-show-needs"
    ]
  }
```
