# API Documentation

## Endpoints

### GET /

#### Description
Retrieves a list of all mods.

#### Response
- **200 OK**

```
{
  "data": [
    {
      //mod data
    },
    {
      //mod data
    }
  ]
} 

```

### GET /search/name/:name

#### Description
Search mod by name.

#### Parameters
- **name**: string

#### Response
- **200 OK**

```
{
  "data": [
    {
      //mod data
    },
    {
      //mod data
    }
  ]
}  
```

### GET /:id

#### Description
Retrieves a mod by id.

#### Parameters
- **id**: string

#### Response
- **200 OK**

```
{
  "data": {
    //mod data
  }
}
```
