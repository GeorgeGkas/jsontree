# Empty Array examples

*document.json*
```json
[]
```

## JSONTree with location information:
*jsontree.json*
```json
{
  "node": {
    "elements": [],
    "loc": {
      "end": {
        "column": 2,
        "line": 1
      },
      "start": {
        "column": 0,
        "line": 1
      }
    },
    "type": "Array"
  }
}
```

## JSONTree with range information:
*jsontree.json*
```json
{
  "node": {
    "elements": [],
    "range": [0, 2],
    "type": "Array"
  }
}
```

## JSONTree with location and range information:
*jsontree.json*
```json
{
  "node": {
    "elements": [],
    "loc": {
      "end": {
        "column": 2,
        "line": 1
      },
      "start": {
        "column": 0,
        "line": 1
      }
    },
    "range": [0, 2],
    "type": "Array"
  }
}
```

## JSONTree without location and range information:
*jsontree.json*
```json
{
  "node": {
    "elements": [],
    "type": "Array"
  }
}
```
