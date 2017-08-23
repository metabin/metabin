![](/_banner.png)

Sharing can be simpler, more effective, more distributed.

The goal is to create a self-sufficient file sharing ecosystem for next-generation distributed apps, where decentralization does not harm user experience and functionality.

## Table of Contents

- [Problem](#problem)
- [Proposal](#proposal)
- [Project structure](#project-structure)
- [Follow us](#follow-us)
- [License](#license)

## Problem

Today's BitTorrent-based ecosystem is stuck. Protocol itself is not very suitable for global-scale sharing but there is also cummunity-related issues we need to solve.


### Torrent-catalogs dependence

BitTorrent designed to handle distributed downloads, but links typicaly shared within a special web-catalogs. There is no reliable distributed and user-friendly alternative for torrents discovery.

![](/images/torrent-catalogs-dependence.png)

What will happen if this torrent-catalog get offline for some reason? Download-guy will continue downloading because he is already directly connected to share-guy. But from this moment for anyone else there is no (easy) way to find this torrent unless it get published somewhere else.

---

### Lack of metadata

Another reason why torrent-catalogs emmerged. BitTorrent is all about file sharing, therefore all related metadata such as artist's info, posters, trailers usually placed on catalog's web-pages.

![](/images/lack-of-metadata.png)

It's possible to place all necessary metadata inside of a torrent and describe it in a standardized way. But because of protocol itself (mostly **Torrent-limited scale** issue described next) such approach leads to unnecessary data duplication and it will be difficult to maintain in general.

---

### Torrent-limited scale

If copies of the same file come across several different torrents, they still do not complement each other as an alternative sources for those who download this file.

![](/images/torrent-limited-scale.png)

*The same applies to torrents with copies of the same file named differently.*

Because of this you can easily end up in a situation, when torrent you interested in has no online seeds, but same files are available under several different torrents with large swarms. And you have to manually crawl different web-ctalogs untill you meet some of this active torrents.

#### proposal

- File sharing ecosystem must move towards IPFS. It has different architecture with no *torrent-limited scale* problem.

---

It's easy to see that current BitTorrent ecosystem scale became possible mostly because of torrent-catalogs - centralized and therefore highly vulnerable resources.

## Proposal

This propblems are possible to solve, in fact some of them already are. Here is some proposals we believe make file sharing great again.


- Files and all related metadata must be shared together.

- Metadata must include as many information as it required to display a high-quality preview.

- Data must be standardized across the sharing space. Therefore community-developed schemas needed. Schemas will act as an agreement between those who share and those who develop distributed apps on how shared data should be described.

## Project structure

- [Metabin schema](https://github.com/metabin/metabin-schema)

Set of libraries and services for community-driven developing and maintaining of data schemas.

- [Metabin share](https://github.com/metabin/metabin-client)

Desktop cli and gui applications that makes it possible to share you local files in IPFS using metabin data schemas.

## Follow us

- Twitter: [@MetabinSpace](http://twitter.com/MetabinSpace)
- Telegram: [@metabin](http://t.me/metabin)
- VK: [@metabin](http://vk.com/metabin)

# License
MIT
