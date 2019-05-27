This document specifies the core JSONTree node types.

- [Node Objects](#node-objects)
  - [Source Location info](#source-location-info)
  - [Source Range info](#source-range-info)
  - [Characters counting in JSON documents](#characters-counting-in-json-documents)
- [Literal Name](#literal-name)
- [String](#string)
- [Number](#number)
- [Array](#array)
- [Object](#object)
- [Member](#member)

### Node Objects

JSONTree nodes are represented as `Node` objects, which may have any prototype inheritance but which implement the following interface:

```js
interface Node {
  type: string
  loc?: SourceLocation
  range?: SourceRange
}
```

The `type` field is a string representing the type of JSONTree variant. Each subtype of `Node` is documented below with the specific string of its type field. You can use this field to determine which interface a node implements.

### Source Location info

The `loc` field represents the source location information of the node. It is an optional object consisting of a `start` position (the position of the first grapheme of the parsed source region) and an `end` position (the position of the first grapheme after the parsed source region).

```ts
interface SourceLocation {
  /**
   * The position of the first grapheme after the parsed source region.
   */
  readonly end: Position

  /**
   * The position of the first grapheme of the parsed source region.
   */
  readonly start: Position
}
```

Each Position object consists of a `line` number (1-indexed) and a `column` number (0-indexed).

```ts
interface Position {
  /**
   * Column number (0-indexed).
   */
  readonly column: number

  /**
   * Line number (1-indexed).
   */
  readonly line: number
}
```

### Source Range info

The `range` field represents the source range information. It is an optional two-value array consisting of a start position (the position of the first grapheme of the parsed source region) and an end position (the position of the first grapheme after the parsed source region). The range values are 0-indexed.

```ts
type indexStart = number
type indexEnd = number
type SourceRange = [indexStart, indexEnd]
```

### Characters counting in JSON documents

[RFC8259 section 8.1](https://tools.ietf.org/html/rfc8259#section-8.1) requires ONLY the use of UTF-8 encoded characters (as defined in [RFC3629](https://tools.ietf.org/html/rfc3629)) in all JSON transmissions that are not part of a closed ecosystem. However, in special occasions, a software that might operates inside an intranet network, the use UTF-16 encoding may be favored.

When dealing with characters outside of Basic Multilingual Plane (U+0000 through U+FFFF), we might end up using surrogate pairs in our documents, for instance the GRINNING FACE character 😀 and/or combining marks. 

Most widely used programming languages do not operate on such grapheme clusters, but on individual code units. Thus the character `😀` is recognized as a string of length two, even if we sense it as a single character. To overcome the problem where different parsers choose to present such characters in different ways, this specification requires that such tools operate on graphemes instead of code units. Thus, a JSON document that contains only the following string value `"😀"` has range `[0, 3]` rather than `[0, 4]`. 

We promote this decision to create a unified behavior among tools that parse and present JSON documents, such as IDEs. It is more natural to specify source locations and ranges by counting graphemes rather than code units.

## Literal Name

Represents a literal name JSON value as defined in [RFC8259 section 3](https://tools.ietf.org/html/rfc8259#section-3).

```js
interface LiteralName extends Node {
  type: 'LiteralName'
  value: true | false | null
  raw: string
}
```

## String

Represents a JSON string value as defined in [RFC8259 section 7](https://tools.ietf.org/html/rfc8259#section-7).

```js
interface String extends Node {
  type: 'String'
  value: string
  raw: string
}
```

## Number

Represents a JSON number value as defined in [RFC8259 section 6](https://tools.ietf.org/html/rfc8259#section-6).

```js
interface Number extends Node {
  type: 'Number'
  value: number
  raw: string
}
```

## Array

Represents a JSON array value as defined in [RFC8259 section 5](https://tools.ietf.org/html/rfc8259#section-5).

```js
interface Array extends Node {
  type: 'Array'
  elements: Array<LiteralName | Array | Object | String | Number>
}
```

## Object

Represents a JSON object value as defined in [RFC8259 section 4](https://tools.ietf.org/html/rfc8259#section-4).

```js
interface Object extends Node {
  type: 'Object'
  members: Member[]
}
```

## Member

Represents a JSON object member as defined in [RFC8259 section 4](https://tools.ietf.org/html/rfc8259#section-4).

```js
interface Member extends Node {
  type: 'Member'
  name: String
  value: LiteralName | Array | Object | String | Number
}
```
