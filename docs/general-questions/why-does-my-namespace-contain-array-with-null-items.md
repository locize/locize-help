# Why does my namespace contain an array with a lot of null items?

When locize serves nested json, it tries to unflatten the keys which by default thinks that key parts beeing numbers, should be items of an array.

Suppose, you have the following keys:

```json
{
    "colors.title": "Colors",
    "colors.enum.0": "red",
    "colors.enum.1": "green",
    "colors.enum.2": "blue"
}
```

This would be published as a nested json like this:

```json
{
    "colors": {
        "title": "Colors",
        "message": [
            "red",
            "green"
            "blue"
        ]
    }
}
```

But sometimes you do no like to have an array.

For example, having these keys:

```json
{
    "error.title": "Errors",
    "error.message.400": "Bad request",
    "error.message.401": "Not authorized",
    "error.message.404": "Not found"
}
```

Would be published as a nested json like this:

```json
{
    "error": {
        "title": "Errors",
        "message": [
            null,
            null,
            null,
            // up to the array index 400...
            "Bad request",
            "Not authorized"
            "Not found"
        ]
    }
}
```

To prevent this add a non-numeric key, like this:

```json
{
    "error.title": "Errors",
    "error.message.unknown": "Unknown error",
    "error.message.400": "Bad request",
    "error.message.401": "Not authorized",
    "error.message.404": "Not found"
}
```

This would be published as a nested json like this:

```json
{
    "error": {
        "title": "Errors",
        "message": {
            "unknown": "Unknown error",
            "400": "Bad request",
            "401": "Not authorized",
            "404": "Not found"
        }
    }
}
```
