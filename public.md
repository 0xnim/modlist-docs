#  Public API Documentation

## Endpoints

### GET /mods

#### Description
Retrieves a list of all mods has a limit of 100 at a time.

#### Example
/mods?limit=5&offset=0

#### Response
- **200 OK**

```
[
	{
		"modID": " SFS_ESM_Utility",
		"modName": "PicoSpace Industries' Utility Pack",
		"modDescription": "Spaceflight Simulator Custom Part Pack with some Utilities that expand the experiance but don't break game mechanics.",
		"modAuthor": "PicoSpace",
		"modVersion": null,
		"modReleaseDate": null,
		"modTags": null,
		"modIcon": null
	},
	{
		"modID": "BASP",
		"modName": "BR-Apollo",
		"modDescription": "Countless detailed, researched, and accurate parts to recreate the Apollo program with.",
		"modAuthor": "Brioche",
		"modVersion": "1.2",
		"modReleaseDate": null,
		"modTags": "recreation, apollo, saturn, parts",
		"modIcon": null
	},
	{
		"modID": "Better-RCS",
		"modName": "Better RCS",
		"modDescription": "Add a lot of RCS with unbelievable power such as RCS titan with Titan power and RCS controlls.",
		"modAuthor": "VTplayz",
		"modVersion": null,
		"modReleaseDate": null,
		"modTags": null,
		"modIcon": null
	},
	{
		"modID": "BuildSettings",
		"modName": "Build Settings",
		"modDescription": "Build settings window and various changes to build mode. See the GitHub repository for a full list of features.",
		"modAuthor": "StarMods",
		"modVersion": null,
		"modReleaseDate": null,
		"modTags": null,
		"modIcon": null
	},
	{
		"modID": "CLOSEST_APPROACH_LINE",
		"modName": "Closest approach line",
		"modDescription": "This mod adds a closest approach line when navigation is active.",
		"modAuthor": "Altaïr",
		"modVersion": null,
		"modReleaseDate": null,
		"modTags": null,
		"modIcon": null
	}
]

```

### GET /mods/:modID

#### Description
Get a single mod.

#### Example
/search/PartEditorInstaller

#### Response
- **200 OK**


```
{
	"modID": "PartEditorInstaller",
	"modName": "Part Editor Installer",
	"modDescription": "Downloads Part Editor and its dependencies and deletes itself.",
	"modAuthor": "nim",
	"modVersion": "1.0.0",
	"modReleaseDate": "2023-04-29T00:00:00.000Z",
	"modTags": "installer",
	"modIcon": null
}
```

### GET /mods/:modID/versions

#### Description
Get all versions of a specific mod.

#### Example
/mods/PartEditorInstaller/versions

#### Response
- **200 OK**

```
[
	{
		"modVersionID": 3,
		"modID": "PartEditorInstaller",
		"versionNumber": "1.0.0",
		"releaseDate": "2023-04-29T00:00:00.000Z",
		"changelog": "Initial Release"
	}
]
```

### GET /mods/:modID/versions/:versionNumber

#### Description
Get a specific version of a mod.

#### Example
/mods/PartEditorInstaller/versions

#### Response
- **200 OK**

```
[
	{
		"modVersionID": 3,
		"modID": "PartEditorInstaller",
		"versionNumber": "1.0.0",
		"releaseDate": "2023-04-29T00:00:00.000Z",
		"changelog": "Initial Release"
	}
]
```
