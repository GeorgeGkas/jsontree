# Number examples

*document.json*
```json
10.5e-5
```

## JSONTree with location information:
*jsontree.json*
```json
{
  "node": {
    "loc": {
      "end": {
        "column": 7,
        "line": 1
      },
      "start": {
        "column": 0,
        "line": 1
      }
    },
    "raw": "10.5e-5",
    "type": "Number",
    "value": 10.5e-5
  }
}
```

## JSONTree with range information:
*jsontree.json*
```json
{
  "node": {
    "range": [0, 7],
    "raw": "10.5e-5",
    "type": "Number",
    "value": 10.5e-5
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
        "column": 7,
        "line": 1
      },
      "start": {
        "column": 0,
        "line": 1
      }
    },
    "range": [0, 7],
    "raw": "10.5e-5",
    "type": "Number",
    "value": 10.5e-5
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
