#  Public API Documentation

## Endpoints

### GET /health

#### Description
Check if the API is online.

#### Example
/health

#### Response
- **200 OK**

```
{
	"message": "Healthy"
}
```


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
/mods/PartEditorInstaller/versions/1.0.0

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

### GET /versions/:versionID/files

#### Description
Get all files for a specific version.

#### Example
/versions/3/files

#### Response
- **200 OK**

```
[
	{
		"fileID": 1,
		"modVersionID": "3",
		"fileType": "mod",
		"fileSize": 6656,
		"fileURL": "https://github.com/Nim1com/ModInstallerList/releases/download/PartEditor/PartEditorInstaller.dll",
		"uploadDate": "2023-05-01T00:00:00.000Z"
	}
]
```

### GET /files/:fileID

#### Description
Get a specific file.

#### Example
/files/1

#### Response
- **200 OK**

```
[
	{
		"fileID": 1,
		"modVersionID": "3",
		"fileType": "mod",
		"fileSize": 6656,
		"fileURL": "https://github.com/Nim1com/ModInstallerList/releases/download/PartEditor/PartEditorInstaller.dll",
		"uploadDate": "2023-05-01T00:00:00.000Z"
	}
]
```

### GET /versions/:versionID/dependencies

#### Description
Get all dependencies for a specific version.

#### Example
/versions/3/dependencies

#### Response
- **200 OK**

```
[
	{
		"id": 2,
		"modVersionID": "3",
		"dependencyModID": "UITools",
		"minimumDependencyVersion": "1.0.0",
		"maximumDependencyVersion": "1.0.0",
		"dependencyType": "required"
	}
]
```

### GET /all/:modID/:versionNumber

#### Description
Get everything required to install a specific mod version.

#### Example
/all/PartEditorInstaller/1.0.0?dependencies=optional

#### Response
- **200 OK**

```
{
	"mod": {
		"modID": "PartEditorInstaller",
		"modName": "Part Editor Installer",
		"modDescription": "Downloads Part Editor and its dependencies and deletes itself.",
		"modAuthor": "nim",
		"modVersion": "1.0.0",
		"modReleaseDate": "2023-04-29T00:00:00.000Z",
		"modTags": "installer",
		"modIcon": null
	},
	"version": {
		"modVersionID": 3,
		"modID": "PartEditorInstaller",
		"versionNumber": "1.0.0",
		"releaseDate": "2023-04-29T00:00:00.000Z",
		"changelog": "Initial Release"
	},
	"files": [
		{
			"fileID": 1,
			"modVersionID": "3",
			"fileType": "mod",
			"fileSize": 6656,
			"fileURL": "https://github.com/Nim1com/ModInstallerList/releases/download/PartEditor/PartEditorInstaller.dll",
			"uploadDate": "2023-05-01T00:00:00.000Z"
		}
	],
	"dependencies": [
		{
			"id": 2,
			"modVersionID": "3",
			"dependencyModID": "UITools",
			"minimumDependencyVersion": "1.0.0",
			"maximumDependencyVersion": "1.0.0",
			"dependencyType": "required"
		}
	]
}
```