# Object examples

*document.json*
```json
{
  "hello": "world"
}
```

## JSONTree with location information:
*jsontree.json*
```json
{
  "node": {
    "loc": {
      "end": {
        "column": 1,
        "line": 3
      },
      "start": {
        "column": 0,
        "line": 1
      }
    },
    "members": [
      {
        "loc": {
          "end": {
            "column": 18,
            "line": 2
          },
          "start": {
            "column": 2,
            "line": 2
          }
        },
        "name": {
          "loc": {
            "end": {
              "column": 9,
              "line": 2
            },
            "start": {
              "column": 2,
              "line": 2
            }
          },
          "raw": "\"hello\"",
          "type": "String",
          "value": "hello"
        },
        "type": "Member",
        "value": {
          "loc": {
            "end": {
              "column": 18,
              "line": 2
            },
            "start": {
              "column": 11,
              "line": 2
            }
          },
          "raw": "\"world\"",
          "type": "String",
          "value": "world"
        }
      }
    ],
    "type": "Object"
  }
}
```

## JSONTree with range information:
*jsontree.json*
```json
{
  "node": {
    "members": [
      {
        "name": {
          "range": [11, 4],
          "raw": "\"hello\"",
          "type": "String",
          "value": "hello"
        },
        "range": [20, 4],
        "type": "Member",
        "value": {
          "range": [13, 20],
          "raw": "\"world\"",
          "type": "String",
          "value": "world"
        }
      }
    ],
    "range": [0, 22],
    "type": "Object"
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
        "column": 1,
        "line": 3
      },
      "start": {
        "column": 0,
        "line": 1
      }
    },
    "members": [
      {
        "loc": {
          "end": {
            "column": 18,
            "line": 2
          },
          "start": {
            "column": 2,
            "line": 2
          }
        },
        "name": {
          "loc": {
            "end": {
              "column": 9,
              "line": 2
            },
            "start": {
              "column": 2,
              "line": 2
            }
          },
          "range": [11, 4],
          "raw": "\"hello\"",
          "type": "String",
          "value": "hello"
        },
        "range": [20, 4],
        "type": "Member",
        "value": {
          "loc": {
            "end": {
              "column": 18,
              "line": 2
            },
            "start": {
              "column": 11,
              "line": 2
            }
          },
          "range": [13, 20],
          "raw": "\"world\"",
          "type": "String",
          "value": "world"
        }
      }
    ],
    "range": [0, 22],
    "type": "Object"
  }
}
```

## JSONTree without location and range information:
*jsontree.json*
```json
{
  "node": {
    "members": [
      {
        "name": {
          "raw": "\"hello\"",
          "type": "String",
          "value": "hello"
        },
        "type": "Member",
        "value": {
          "raw": "\"world\"",
          "type": "String",
          "value": "world"
        }
      }
    ],
    "type": "Object"
  }
}
```
