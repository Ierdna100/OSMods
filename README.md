# OSMods
Repository of currently registered Obenseuer mods to be referenced externally.

# Registering your mod
In order to add a mod you have created onto the list, you must make a [Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) and modify mods.json to include your mod. The PR will be checked for proper JSON formatting and will then be pulled (hopefully automatically in the near future).

Example Structure of a mod (for details, please have a look at the schema present in this same repository):
```json
{
  "id": "owner.product",
  "displayName": "A Name The End-User Will See",
  "tagline": "Best Mod on the Market",
  "description": null, // Can be removed entirely for the time being
  "owner": "your-github-name", 
  "repository": "repository-unique-identifier", 
  "releases": {
    "0.4.01": [
      "1.0.0"
    ]
  },
  "dependencies": [ 
      "always-show-needs"
  ]
}
```
