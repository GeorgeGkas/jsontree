# Strings examples

*document.json*
```json
"hello 😀"
```

## JSONTree with location information:
*jsontree.json*
```json
{
  "node": {
    "loc": {
      "end": {
        "column": 9,
        "line": 1
      },
      "start": {
        "column": 0,
        "line": 1
      }
    },
    "raw": "\"hello 😀\"",
    "type": "String",
    "value": "hello 😀"
  }
}
```

## JSONTree with range information:
*jsontree.json*
```json
{
  "node": {
    "range": [0, 9],
    "raw": "\"hello 😀\"",
    "type": "String",
    "value": "hello 😀"
  }
}
```

## JSONTree with location and range information:
*jsontree.json*
```json
{
  "node": {
    "loc": {
      "end": {
        "column": 9,
        "line": 1
      },
      "start": {
        "column": 0,
        "line": 1
      }
    },
    "range": [0, 9],
    "raw": "\"hello 😀\"",
    "type": "String",
    "value": "hello 😀"
  }
}
```

## JSONTree without location and range information:
*jsontree.json*
```json
{
  "node": {
    "raw": "10.5e-5",
    "type": "Number",
    "value": 10.5e-5
  }
}
```
