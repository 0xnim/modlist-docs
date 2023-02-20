# Versions API Documentation

## Endpoints /api/versions

### GET /mod/:identifier

#### Description
Retrieves a list of all versions for a specific mod.

#### Parameters
- **identifier**: string

#### Example
/mod/parteditor

#### Response
- **200 OK**

```
{
	"data": [
		{
			"id": 2,
			"identifier": "parteditor",
			"version": "v1.0.0",
			"download": "https://github.com/cucumber-sp/PartEditor/releases/download/v1.0/PartEditor.dll",
			"hash": "7ef663d2dabffad93bb271b39928cb4d",
			"game_version": "1.5.9.6",
			"dependencies": "1",
			"type": "mod"
		},
		{
			"id": 5,
			"identifier": "parteditor",
			"version": "Beta-0.9.2",
			"download": "https://github.com/cucumber-sp/PartEditor/releases/download/Beta-0.9.2/PartEditor.dll",
			"hash": "d58496f1e9a580be19165938b0cc81c0",
			"game_version": "1.5.7",
			"dependencies": null,
			"type": "mod"
		},
		{
			"id": 6,
			"identifier": "parteditor",
			"version": "Beta-0.9.1",
			"download": "https://github.com/cucumber-sp/PartEditor/releases/download/Beta-0.9.1/PartEditor.dll",
			"hash": "bbef384a058ebf5b6ea766c3ee6630d4",
			"game_version": "0.5.7",
			"dependencies": null,
			"type": "mod"
		}
	]
}
```


### GET /id/:id

#### Description
Retrieves a version by id.

#### Parameters
- **id**: string

#### Example
/id/2

#### Response
- **200 OK**

```
{
	"data": {
		"id": 2,
		"identifier": "parteditor",
		"version": "v1.0.0",
		"download": "https://github.com/cucumber-sp/PartEditor/releases/download/v1.0/PartEditor.dll",
		"hash": "7ef663d2dabffad93bb271b39928cb4d",
		"game_version": "1.5.9.6",
		"dependencies": "1",
		"type": "mod"
	}
}
```
