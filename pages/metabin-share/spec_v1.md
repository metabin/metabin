# Metabin Share specification

Version 1

## Table of contents

- [Api](#api)
  - [Put metabin object](#put-metabin-object)
  - [Get metabin object](#get-metabin-object)
- [License](#license)

## Api

### Put metabin object

- arguments:
  - metabin object candidate
  - options
    - `put anyway` flag, default is false
- returns:
  - `valid` flag (always)
  - array with validator reports (always)
  - `cid` string field (always if `put anyway` is true, otherwise only if object is valid)

### Get metabin object

- arguments:
  - cid string
  - options:
    - `pin anyway` flag, default is false
- returns:
  - `valid` flag (always)
  - array with validator reports (always)
  - metabin object (always)

## License

MIT
