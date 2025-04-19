---
layout: post
title: Getting Started with Payload 3 Localization Boilerplate
---

<!-- <mark>Update: 19 Apr 2025 -->

<!-- The _Finder_ is MacOS' equivalent to _Windows Explorer_ and is handy to use due to useful systemwide shortcuts. -->

I have finally found a good starting point for the development of a multilingual Payload 3 website. So far I have found it difficult to find a good way to implement multilingualism ‘correctly’ in Payload. Unfortunately, in my opinion, the documentation here is not in-depth enough or I lack the necessary skills.
But I have now found a template that is based on the Payload Webiste template and already has multilingualism integrated. This example can be found in the regular payload repository and I would like to briefly summarise how the individual steps work.

---

## Installation

You can either clone the corresponding repository [Repository](https://github.com/payloadcms/payload/tree/main/examples/localization) or simply install it from scratch:

`npx create-payload-app --example localization`
<br>_(clone the localization example)_

`cp .env.example .env`
<br>_(generate .env file)_

`pnpm install`
<br>_(install all dependencies via pnpm (don't use npm))_

`docker compose up`
<br>_(set up local database)_

`pnpm run dev`
<br>_(run development server)_

---

## Sidenotes

1. <b>pnpm instead of npm:</b><br>I first tried to use _npm_ as my regular package manager here. It caused too much trouble so I gave _pnpm_ a try and all the dependenciy issues were gone.

2. <b>Issue with "sharp" module:</b><br>I went into issues with the sharp module when running `pnpm dev`. The following additional lines to the `package.json` fixed it for me:<br><br><code>"pnpm": {<br>
   "overrides": {<br>
   "sharp": "0.33.5"<br>
   }<br>
   }</code>
