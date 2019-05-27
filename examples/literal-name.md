# Literal Name examples

*document.json*
```json
true
```

## JSONTree with location information:
*jsontree.json*
```json
{
  "node": {
    "loc": {
      "end": {
        "column": 4,
        "line": 1
      },
      "start": {
        "column": 0,
        "line": 1
      }
    },
    "raw": "true",
    "type": "LiteralName",
    "value": true
  }
}
```

## JSONTree with range information:
*jsontree.json*
```json
{
  "node": {
    "range": [0, 4],
    "raw": "true",
    "type": "LiteralName",
    "value": true
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
        "column": 4,
        "line": 1
      },
      "start": {
        "column": 0,
        "line": 1
      }
    },
    "range": [0, 4],
    "raw": "true",
    "type": "LiteralName",
    "value": true
  }
}
```

## JSONTree without location and range information:
*jsontree.json*
```json
{
  "node": {
    "raw": "true",
    "type": "LiteralName",
    "value": true
  }
}
```
