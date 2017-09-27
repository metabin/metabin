# Metabin Schemas

BitTorrent sharing space is a mess. To make it more structured, predictable and easy to search special web-catalogs emmerged (The Pirate Bay, ISOHunt).

For IPFS-like sharing space there is no need in such centralized resources. Instead we are able to describe what we share with schemas. It becomes possible to describe complex interrelations between shared files and their metadata in a predictable yet fully distributed maner. Therefore modern apps will be able to search, find, validate and display user-friendly previews for such complex entities as modular movies without any server.

It's like if `.torrent` files came with all necessary metadata that usually put on catalog's web-pages e.g. posters, genres, trailers, author's info and so on.

## Table of Contents

- [Roadmap](#roadmap)
- [Schema types](#schema-types)
- [Examples](#examples)
- [License](#license)

## Roadmap

- [ ] web-site for schemas development
- [x] validation libs
  - [x] [js](https://github.com/metabin/metabin-schema-validator-js)

## Schema types

Types listed below can be used to declare a schema fields.

Type | Declaring | Value expample
------------ | ------------- | -------------
text string | `"string"` | `"Another Pirated Movie Title"`
number | `"number"` | `2017`
boolean | `"boolean"` | `false`
ENUM value | `[[ "E", "N", "U", "M" ]]` |  `0` or `1` or `2` or `3`

Also schema field can store a nested schema in a form of a simple object with it's own fields.

```json
{
  "field": "string",
  "nested": {
    "field: "boolean"
  }
}
```

Also it's possible to declare an array of a single type.

```json
{
  "field": ["string"]
}
```

## Examples

Any schema looks like an associative dictionary of `field_name : field_type` pairs. Anyone who uses such a schema should follow this dictionary to describe all necessary metadata for published data.

```json
{
  "title": "string",
  "director": {
    "first name": "string",
    "last name": "string"
  },
  "year": "number",
  "genre": [[ "LIVE ACTION", "DOCUMENTARY", "ANIMATION" ]],
  "trailer": "string",
  "video": [
    {
      "quality": [[ ... "720p", "1080p", "4k" ]],
      "source": "string"
    }
  ],
  "audio": [
    {
      "quality": [[ ... "AC3", "DTS" ]],
      "language": "string",
      "original": "boolean",
      "source": "string"
    }
  ],
  "subtitles": [
    {
      "language": "string",
      "source": "string"
    }
  ]
}
```

This is example of schema that can be used to describe an entity we call "modular movie". It describes a movie that splited into logical pieces so it becomes possible to download / stream a movie with video, audio, language settings that suits your needs (`720p + AC3 portugal audio + korean subs` or `1080p + DTS english audio`). And no extra MB will be downloaded!

Any entity object can be easilly extended so it's possible for community to maintain a `modular-movie` objects to still up-to-date and include all known translations, video-formats, subtitles and so on.

```json
{
  "title": "string",
    "artist": {
      "title": "string",
      "members": [
        {
          "first name": "string",
          "last name": "string",
          "pseudonym": "string"
        }
      ]
    },
    "year": "number",
    "format": [[ "SINGLE", "LIVE", "STUDIO", "EP" ]],
    "cover": [
      {
        "size": [[ "SMALL", "MEDIUM", "LARGE" ]],
        "source": "string"
      }
    ],
    "tracks": [ 
      {
        "title": "string",
        "quality": [[ "web", "cd", "vinyl" ]]
      }
    ]
}
```

Here is another example of modular entity. Albums shared with schema like this are possible to download with any qulaity or to adjust audio stream on the fly. Spotify is limited with 320kbps for premium users, community sharing has no limits. Switch from 128kbps to Vinyl Rip quality if such is available and your banwidth is enough.

## License

MIT
