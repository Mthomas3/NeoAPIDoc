# Admin media update
**[HOME](../README.md)**

**URL** : `/admin/media/update`

**Method** : `PUT`

**Authentication required** : YES (JWT token)

**Permissions required** : Admin

**Description :**
Update data of a given media

Informations to provide :

```json
{
  "token | device_token": "[string]",
  "media_id": "[integer]",
  "filename": "[string] (optional)",
  "extension": "[string] (optional)",
  "identifier": "[string] (optional)",
  "directory": "[string] (optional)"
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
    "success": true
}
```

## Error Responses

**Condition** : Error occured.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "message": "[Error message]",
    "success": false
}
```