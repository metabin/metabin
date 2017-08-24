![](/_banner.png)

Sharing can be simpler, more effective, more distributed.

The goal is to create a self-sufficient file sharing ecosystem for next-generation distributed apps, where decentralization does not harm user experience and functionality.

## Table of Contents

- [Problem](#problem)
- [Project structure](#project-structure)
- [Follow us](#follow-us)
- [License](#license)

## Problems

Today's BitTorrent-based ecosystem is stuck. Protocol itself is not very suitable for global-scale sharing but there is also cummunity-related issues we need to solve.


### Centralized torrent's discovery
 
BitTorrent designed to handle distributed downloads, but links typicaly shared within a special web-catalogs (The Pirate Bay, ISOHunt and so on). There is no reliable distributed and user-friendly alternative for torrents discovery.

![](/images/torrent-catalogs-dependence.png)

What will happen if this torrent-catalog get offline for some reason? Download-guy will continue downloading because he is already directly connected to share-guy. But from this moment for anyone else there is no (easy) way to find this torrent unless it get published somewhere else.

#### Proposal

- There must be a fully distributed yet easy and effective way to discover shared data instances. It's possible to achieve using, for example, IPFS pub/sub channels. This makes possible to build, for instance, a desktop media-player that autodiscovers new albums shared by others not relying on any third-party resources.

---

### Lack of standardized metadata

Content-related metadata such as artist's info, posters, trailers almost never included in .torrent files. Such data typicaly considered as unnecessary and placed on dedicated catalog's web-pages.

![](/images/lack-of-metadata.png)

It's possible to place all necessary metadata inside of a torrent and describe it in a standardized way. But because of protocol itself (mostly **Torrent-limited scale** issue described next) such approach leads to unnecessary data duplication and it will be difficult to maintain in general.

Another problem is standardization of data across the sharing space. How will application identify what kind of entity it found? Is it a musical album or audio book? Folder structure differs across torrents with same type of content, the same is for file names.

#### Proposal

- Files and all related metadata must be shared together as a single instance. This makes possible to build an informative high-quality previews of such instances based only on their own content.
- Data structure of such instances must be standardized using community-developed schemas. Schemas will act as an agreement between those who share and those who develop distributed apps on how data should be described.

---

### Torrent-limited scale

If copies of the same file come across several different torrents, they still do not complement each other as an alternative sources for those who download this file.

![](/images/torrent-limited-scale.png)

*The same applies to torrents with copies of the same file named differently.*

Because of this you can easily end up in a situation, when torrent you interested in has no online seeds, but same files are available under several different torrents with large swarms. And you have to manually crawl different web-ctalogs untill you meet some of this active torrents.

#### Proposal

-  File sharing ecosystem must move towards IPFS. It has different architecture with a single content-addresded sharing space. Moreover it gives an ability to easilly describe complex relations between files and their metadata within a single graph.

---
 
## Project structure

- [Metabin schema](https://github.com/metabin/metabin-schema)

Set of libraries and services for community-driven developing and maintaining of data schemas.

- [Metabin share](https://github.com/metabin/metabin-client)

Desktop cli and gui applications that makes it possible to share you local files using community-developed data schemas.

## Follow us

- Twitter: [@MetabinSpace](http://twitter.com/MetabinSpace)
- Telegram: [@metabin](http://t.me/metabin)
- VK: [@metabin](http://vk.com/metabin)

# License
MIT
