# Metabin Object specification

Version 1

## Table of contents

- [Root object](#root-object)
- [Data types](#data-types)
- [Array of type](#array-of-type)
- [Nested objects](#nested-objects)
- [License](#license)

## Root object

Root object consists of thre fields:
- `schema` field
  - stores an object that describes structure of `data` object
- `data` field
  - stores an object that describes an instance of a `shema`
- `metabin` field
  - stores a string with a compatible metabin object spec version

Example:

```json
{
  "schema": {
    "field": "number"
  },
  "data": {
    "field": 13
  },
  "metabin": "1"
}
```

## Data Types

Type | Declaring | Value example
------------ | ------------- | -------------
text string | `"string"` | `"Another Pirated Movie Title"`
number | `"number"` | `2017`
boolean | `"boolean"` | `false`
ENUM value | `[[ "E", "N", "U", "M" ]]` |  `0` or `1` or `2` or `3`

## Array of type

Example:

```json
{
  "schema": {
    "field": [ "string" ]
  },
  "data": {
    "field": [ "some", "text", "here" ]
  }
}
```

- Allowed data types
  - `number`
  - `string`
  - `boolean`
- Nested object is allowed
- Only single type / object allowed

## Nested objects

Example:

```json
{
  "schema": {
    "field": "string",
    "nested": {
      "field": "boolean"
    }
  },
  "data": {
    "field": "some text",
    "nested": {
      "field": false
    }
  }
}
```

## License

MIT
