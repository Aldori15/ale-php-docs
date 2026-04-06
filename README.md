# Eluna / ALE API Docs

A plug-and-play, self-hosted PHP documentation browser for [Eluna](https://github.com/ElunaLuaEngine/Eluna) and [ALE](https://github.com/azerothcore/mod-ale) — parses your `.h` method headers directly, no build step required.

---

## Features

- **Plug-and-play** — point it at your headers directory and it works
- **Inheritance tree** — subclasses show inherited methods with source attribution
- **Live search** — instant search across all classes and methods
- **Auto-parsed docs** — `@param`, `@return`, `@proto`, enum blocks, and inline links all rendered automatically
- **Easily customizable** — single CSS file, straightforward PHP partials

---

## Screenshots

**Full site**

<img width="1651" alt="Full site" src="https://github.com/user-attachments/assets/ca8d7a34-d9f0-4b82-b0d9-2653d95e909f" />
<br><br>

**Inheritance — inherited methods shown in subclasses**

<img width="1065" alt="Inheritance" src="https://github.com/user-attachments/assets/e23b40bf-2d31-4b18-a9f2-219823ceeb9a" />
<br><br>

**Search**

<img width="544" alt="Search" src="https://github.com/user-attachments/assets/1928dd2f-a224-4235-93aa-5963f88c19fb" />

---

## Setup

1. Clone the repo into your web server's document root.
2. Edit `config.php` and set `headers_dir` to your Eluna/ALE methods directory. You can, for example, git clone mod-ale directly into this dir to have it work right out of the box.
3. Done.

Optionally, you may also fork this repository and set up GitHub Pages to make static HTML copies of the docs for your personal Eluna/ALE version, by editing the sources array in `generate_github_docs.php`.

---

## Roadmap

- [X] File-based caching. Parse once, serve statically instead of re-parsing on every request.
- [X]  ~~Hashing/target dir size check to re-cache on methods dir changes.~~ GitHub Pages pull from sources every 24 hours, and users can optionally set up re-fetching of local source files.
