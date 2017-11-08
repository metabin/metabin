# Metabin Schema specification

Version 1

## Table of contents

- [Spec field](#spec-field)
- [Data types](#data-types)
- [Array of type](#array-of-type)
- [Nested objects](#nested-objects)
- [License](#license)

## Spec field

To mark current json-object as a metabin schema use a "$spec" field with a `"metabin/${version number}"` value pattern.

```json
{
  "schema": {
    "$spec": "metabin/1"
  }
}
```

## Data Types

Type | Declaring | Value example
------------ | ------------- | -------------
text string* | `"string"` | `"Another Pirated Movie Title"`
number | `"number"` | `2017`
boolean | `"boolean"` | `false`
ENUM value | `[[ "E", "N", "U", "M" ]]` |  `0` or `1` or `2` or `3`

*empty string `""` considered as an invalid string value

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
