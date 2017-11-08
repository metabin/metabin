
# Metabin Object schema example

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
