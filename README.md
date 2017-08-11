![](/_banner.png)

Sharing can be simpler, more effective, more distributed.

The goal is to create a self-sufficient file sharing ecosystem for next-generation distributed apps, where decentralization does not harm user experience and functionality.

## Table of Contents

- [Project structure](#project-structure)
- [Core ideas](#core-ideas)
- [Problem](#problem)
- [Follow us](#follow-us)
- [License](#license)

## Project structure

- [Metabin schema](https://github.com/metabin/metabin-schema)

Set of libraries and services for community-driven developing and maintaining of data schemas.

- [Metabin share](https://github.com/metabin/metabin-client)

Desktop cli and gui applications that makes it possible to share you local files in IPFS using metabin data schemas.

## Core ideas

- **Filesystem as API**

To publish a file all you need is to create a same name `.meta` file in the same place.

[details](/docs/fs-as-api/doc.md)

- **Combined publications**

Publications can be combined in a higher-level publications. For example, separately published audio-files can be also published together as an album.

[details](/docs/combined/doc.md)

- **Metadata included**

Aside of pointing to the published files, .meta files store related metadata. In case of audio-file it can be track number, artist name an so on.

[details](/docs/metadata/doc.md)

- **Community developed meta-schemas**

Stored in .meta files metadata must be standartized, so it can be recognized by apps. It can be achived with a special `!schema` key, placed in a `.meta` file (for ex `"!shema": "music-album:v1"`).

[details](/docs/schemas/doc.md)

## Follow us

- Twitter: [@MetabinSpace](http://twitter.com/MetabinSpace)
- Telegram: [@metabin](http://t.me/metabin)
- VK: [@metabin](http://vk.com/metabin)

# License
MIT
