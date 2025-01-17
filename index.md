---
layout: page
title: "Home"
ignore_title: true
tags: ["decentralized", "decentralised", "database", "p2p", "peer-to-peer", "web", "ipfs", "haja", "orbit", "orbitdb"]
excerpt: "Peer-to-Peer Databases for the Decentralized Web"
search_omit: true
---

<h2 class="site-description center" itemprop="description">Peer-to-Peer Databases for the Decentralized Web</h2>

<p class="center"><a href="https://gitter.im/orbitdb/Lobby"><img src="https://img.shields.io/gitter/room/nwjs/nw.js.svg" alt="Gitter"/></a> <a href="https://circleci.com/gh/orbitdb/orbit-db" alt="CircleCI Status"><img src="https://circleci.com/gh/orbitdb/orbit-db.svg?style=shield" /></a>
<a href="https://www.npmjs.com/package/orbit-db" alt="npm version"><img src="https://badge.fury.io/js/orbit-db.svg" /></a>
<a href="https://www.npmjs.com/package/orbit-db" alt="node"><img src="https://img.shields.io/node/v/orbit-db.svg" /></a></p>

OrbitDB is a serverless, distributed, peer-to-peer database. OrbitDB uses [IPFS](https://ipfs.io) as its data storage and [IPFS Pubsub](https://github.com/ipfs/go-ipfs/blob/master/core/commands/pubsub.go#L23) to automatically sync databases with peers. It's an eventually consistent database that uses [CRDTs](https://en.wikipedia.org/wiki/Conflict-free_replicated_data_type) for conflict-free database merges making OrbitDB an excellent choice for decentralized apps (dApps), blockchain applications and offline-first web applications.

<h2 class="center" id="test">Test it live!</h2>

<p class="center">
<a class="btn btn-demo" href="https://ipfs.io/ipfs/QmeESXh9wPib8Xz7hdRzHuYLDuEUgkYTSuujZ2phQfvznQ/">Live Demo 1</a> 
<a class="btn btn-demo" href="https://ipfs.io/ipfs/QmasHFRj6unJ3nSmtPn97tWDaQWEZw3W9Eh3gUgZktuZDZ/">Live Demo 2</a>
<a class="btn btn-demo" href="https://ipfs.io/ipfs/QmTJGHccriUtq3qf3bvAQUcDUHnBbHNJG2x2FYwYUecN43/">P2P TodoMVC App</a>
</p>

<h2 class="center">Announcements and Updates</h2>
<ul class="post-list">
{% for post in site.posts limit:10 %}
  <li><article><a href="{{ site.url }}{{ post.url }}"><div class="post-entry-title">{{ post.title }}</div> <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt | remove: '\[ ... \]' | remove: '\( ... \)' | markdownify | strip_html | strip_newlines | escape_once }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>
