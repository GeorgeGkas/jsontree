# Array examples

*document.json*
```json
[true, 5]
```

## JSONTree with location information:
*jsontree.json*
```json
{
  "node": {
    "elements": [
      {
        "loc": {
          "end": {
            "column": 5,
            "line": 1
          },
          "start": {
            "column": 1,
            "line": 1
          }
        },
        "raw": "true",
        "type": "LiteralName",
        "value": true
      },
      {
        "loc": {
          "end": {
            "column": 8,
            "line": 1
          },
          "start": {
            "column": 7,
            "line": 1
          }
        },
        "raw": "5",
        "type": "Number",
        "value": 5
      }
    ],
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
    "type": "Array"
  }
}
```

## JSONTree with range information:
*jsontree.json*
```json
{
  "node": {
    "elements": [
      {
        "range": [1, 5],
        "raw": "true",
        "type": "LiteralName",
        "value": true
      },
      {
        "range": [7, 8],
        "raw": "5",
        "type": "Number",
        "value": 5
      }
    ],
    "range": [0, 9],
    "type": "Array"
  }
}
```

## JSONTree with location and range information:
*jsontree.json*
```json
{
  "node": {
    "elements": [
      {
        "loc": {
          "end": {
            "column": 5,
            "line": 1
          },
          "start": {
            "column": 1,
            "line": 1
          }
        },
        "range": [1, 5],
        "raw": "true",
        "type": "LiteralName",
        "value": true
      },
      {
        "loc": {
          "end": {
            "column": 8,
            "line": 1
          },
          "start": {
            "column": 7,
            "line": 1
          }
        },
        "range": [7, 8],
        "raw": "5",
        "type": "Number",
        "value": 5
      }
    ],
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
    "type": "Array"
  }
}
```

## JSONTree without location and range information:
*jsontree.json*
```json
{
  "node": {
    "elements": [
      {
        "raw": "true",
        "type": "LiteralName",
        "value": true
      },
      {
        "raw": "5",
        "type": "Number",
        "value": 5
      }
    ],
    "type": "Array"
  }
}
```
