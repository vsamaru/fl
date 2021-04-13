<img src="https://github.com/flareact/flareact/raw/canary/flareact.png" alt="Flareact" width="350" />

Flareact is an **edge-rendered React framework** powered by Cloudflare Workers.

[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/vsamaru/fl)

It's inspired by [Next.js](https://nextjs.org/).

That means it supports nice API patterns like:

- File-based routing
- Dynamic page paths
- Data fetching for page props using `getEdgeProps`
- API routes
- Universal application rendering (worker and client)

However, it's brand new! So it's also a bunch of these things:

- **It probably does not work on Windows**
- Missing years worth of optimizations the Next.js team has implemented

[Check out the docs!](https://flareact.com)

---
description: Shorten URLs with invisible spaces
---

# Zero Width Shortener

Zero Width Shortener \(abbreviated as ZWS\) is a URL shortener that shortens URLs using spaces that have zero width, making them invisible to humans.

### Characters

We've done a bit of research on what characters work on different platforms

| Character | In use | [Twitter](https://twitter.com/) | [iMessage](https://support.apple.com/explore/messages)\* | [Discord](https://discordapp.com/) | [Slack](https://slack.com) | [Telegram](https://telegram.org/) | Notes |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `U+200B` | ✔️ | ❌ | ❌ | ✔️ | ❌ | ✔️ | Used in URLs since initial release, blacklisted space character on [Twitter](https://twitter.com/) |
| `U+200D` | ✔️ | ❌ |  | ✔️ |  | ✔️ | [Discord](https://discordapp.com/) prompts you with a "spoopy URL" popup when clicked |
| `U+200C` | ❌ | ❌ |  | ✔️ |  | ❌ | Blacklisted space on [Twitter](https://twitter.com/), discontinued \(previously used, replaced with `U+200D`\) |
| `U+180E` | ❌ | ❌ | ❌ | ✔️ |  | ❌ | Visible on iOS, discontinued in b39897e \(previously used, replaced with `U+200C`\) |
| `U+061C` | ❌ | ❌ |  | ✔️ |  | ✔️ |  |

* [iMessage](https://support.apple.com/explore/messages) note: Tested on latest beta of iOS


## Contributors

### Code Contributors

This project exists thanks to all the people who contribute. [[Contribute](CONTRIBUTING.md)].
<a href="https://github.com/zws-im/zws/graphs/contributors"><img src="https://opencollective.com/zws/contributors.svg?width=890&button=false" /></a>

### Financial Contributors

Become a financial contributor and help us sustain our community. [[Contribute](https://opencollective.com/zws/contribute)]

#### Individuals

<a href="https://opencollective.com/zws"><img src="https://opencollective.com/zws/individuals.svg?width=890"></a>
