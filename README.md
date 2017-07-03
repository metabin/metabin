![](/banner.png)

Sharing can be simpler, more effective, more distributed.

## Core ideas
- **Filesystem as API**
To publish a file all you need is to create a same name `.meta` file in the same place.
- **Combined publications**
Publications can be combined in a higher-level publications. For example, separatly published audio-files can be also published together as an album.
- **Metadata included**
Aside of pointing to the published files, .meta files store related metadata. In case of audio-file it can be track number, artist name an so on.
- **Community developed meta-schemas**
Stored in .meta files metadata must be standartized, so it can be properly displayed by apps. It can be achived with a special `!schema` key, placed in a `.meta` file (for ex `"!shema": "music-album:v1"`).

The goal is to create a self-sufficient data sharing platform for next-generation distributed apps, where decentralization does not harm user experience and functionality.

# License
MIT
