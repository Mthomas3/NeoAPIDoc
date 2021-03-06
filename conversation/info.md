# Conversation informations
**[HOME](../README.md)**

**URL** : `/conversation/info/<conversation_id>`

**Method** : `GET`

**Authentication required** : YES (JWT token)

**Permissions required** : User | Device & Being member of the conversation


Informations to provide in header :

```json
{
    "Authorization": "[string]"
}
```

## Success Response

**Condition** : If everything is OK.

**Code** : `200 OK`

**Content example**

```json
{
    "content": {
        "name": "[string(120)]",
        "updated": "[string(datetime)]",
        "created": "[string(datetime)]",
        "device_access": "[boolean]",
        "id": "[integer]",
        "circle": {
            "created": "[string(datetime)]",
            "device": "[integer]",
            "id": "[integer]",
            "name": "[string(120)]",
            "updated": "[string(datetime)]"
        },
        "links": [
            {
                "circle_id": "[integer]",
                "created": "[string(datetime)]",
                "id": "[integer]",
                "privilege": "[string(10)]",
                "updated": "[string(datetime)]",
                "conversation_id": {
                    "circle_id": "[integer]",
                    "created": "[string(datetime)]",
                    "device_access": "[boolean]",
                    "id": "[integer]",
                    "name": "[string(120)]",
                    "updated": "[string(datetime)]"
                },
                "messages": [
                    {
                        "content": "[string(8192)]",
                        "id": "[integer]",
                        "link_id": "[integer]",
                        "medias": "[integer]",
                        "read": "[string(datetime)]",
                        "sent": "[string(datetime)]"
                    }
                ],
                "user_id": {
                    "birthday": "[string(datetime)]",
                    "created": "[string(datetime)]",
                    "email": "[string(120)]",
                    "first_name": "[string(50)]",
                    "id": "[integer]",
                    "isOnline": "[boolean]",
                    "last_name": "[string(50)]",
                    "type": "[string(10)]",
                    "updated": "[string(datetime)]"
                }
            }
        ],
        "messages": [
            {
                "content": "[string(8192)]",
                "id": "[integer]",
                "link_id": "[integer]",
                "medias": "[integer]",
                "read": "[string(datetime)]",
                "sent": "[string(datetime)]"
            }
        ]
    },
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