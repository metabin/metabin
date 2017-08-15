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

BitTorrent ecosystem is stuck. First of all it caused by protocol itslef and it's limited scalability. Here is some main flaws.

- *Torrent-limited scale.* If copies of the same file come across several different torrents, they still do not complement each other as an alternative sources for those who download this file.

- *Torrent-catalogs dependence.* BitTorrent designed to handle distributed downloads, but links typicaly shared within a special web-catalogs. There is no reliable distributed and user-friendly alternative for torrents discovery.

- *Lack of metadata.* Another reason why torrent-catalogs emmerged. BitTorrent is all about file sharing, related metadata such as artist's info, posters, trailers usually placed separately on catalog's web-pages.

It's easy to see that current BitTorrent ecosystem scale became possible mostly because of torrent-catalogs - centralized and therefore highly vulnerable resources.

## Proposal

This propblems are possible to solve, in fact some of them already are. Here is some proposals we believe make file sharing great again.

- File sharing ecosystem must move towards IPFS. It already solved *torrent-limited scale* problem.

- Metadata and actual data (stored in files) must be tied together and shared the same way.

- Metadata must include as many information as it required to display a high-quality preview.

- Data must be standardized across all the sharing space. Therefore community-developed schemas needed that will be used to describe it. Schemas will act as an agreement between those who share and those who develop IPFS-based apps.

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
