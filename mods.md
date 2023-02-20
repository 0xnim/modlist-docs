# Mods API Documentation

## Endpoints /api/mods

### GET /

#### Description
Retrieves a list of all mods.

#### Response
- **200 OK**

```
{
	"data": [
		{
			"id": 1,
			"name": "UI Tools",
			"identifier": "UITools",
			"author": "Cucumber Space",
			"status": 1,
			"description": "A dependency mods to make implementing a lot of quality-of-life features much easier.",
			"type": "mod",
			"downloads": 56942
		},
		{
			"id": 2,
			"name": "Part Editor",
			"identifier": "parteditor",
			"author": "Cucumber Space",
			"status": 1,
			"description": "Edit all part stats in game!",
			"type": "mod",
			"downloads": 23547
		},
		{
			"id": 3,
			"name": "Smart SAS",
			"identifier": "smartsasmod",
			"author": "pixelgaming579",
			"status": 1,
			"description": "Adds a variety of control options for the stability assist system (SAS).",
			"type": "mod",
			"downloads": 4291
		},
		{
			"id": 4,
			"name": "Build Settings",
			"identifier": "BuildSettings",
			"author": "StarMods",
			"status": 1,
			"description": "Build settings window and various changes to build mode. See the GitHub repository for a full list of features.",
			"type": "mod",
			"downloads": 6809
		},
		{
			"id": 5,
			"name": "Closest approach line",
			"identifier": "CLOSEST_APPROACH_LINE",
			"author": "Altaïr",
			"status": 1,
			"description": "This mod adds a closest approach line when navigation is active.",
			"type": "mod",
			"downloads": 2284
		}
  ]
}

```

### GET /search/name/:name

#### Description
Search mod by name.

SQL: WHERE name LIKE %search%

#### Parameters
- **name**: string

#### Example
/search/name/ui

#### Response
- **200 OK**


```
{
	"data": [
		{
			"id": 1,
			"name": "UI Tools",
			"identifier": "UITools",
			"author": "Cucumber Space",
			"status": 1,
			"description": "A dependency mods to make implementing a lot of quality-of-life features much easier.",
			"type": "mod",
			"downloads": 56942
		},
		{
			"id": 4,
			"name": "Build Settings",
			"identifier": "BuildSettings",
			"author": "StarMods",
			"status": 1,
			"description": "Build settings window and various changes to build mode. See the GitHub repository for a full list of features.",
			"type": "mod",
			"downloads": 6809
		}
	]
}
```

### GET /:id

#### Description
Retrieves a mod by id.

#### Parameters
- **id**: string

#### Example
/2

#### Response
- **200 OK**

```
{
	"data": {
		"id": 2,
		"name": "Part Editor",
		"identifier": "parteditor",
		"author": "Cucumber Space",
		"status": 1,
		"description": "Edit all part stats in game!",
		"type": "mod",
		"downloads": 23547
	}
}
```
