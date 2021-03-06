# Metabin Object specification

Version 1

## Table of contents

- [Fields](#fields)
- [Examples](#examples)

## Fields

Metabin object consists of two fields:
- `schema` field
  - stores an object that describes structure of `data` object
- `data` field
  - stores an object that describes an instance of a `schema`

## Examples

Metabin object with a data object and a metabin-schema object.

```json
{
  "schema": {
    "$spec": "metabin/1",
    "field": "number"
  },
  "data": {
    "field": 13
  }
}
```

Metabin object with a data object and a json-schema object.

```json
{
  "schema": {
    "$schema": "http://json-schema.org/draft-06/schema#",
    "type": "object",
    "properties": {
      "field": {
        "type": "number"
      }
    }
  },
  "data": {
    "field": 13
  }
}
```

## License

MIT
