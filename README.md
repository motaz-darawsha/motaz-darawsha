<div align="center">
  <img src="./assets/header.svg" width="100%" alt="header"/>
</div>

<br/>

<div align="center">
  <img src="./assets/status.svg" width="100%" alt="status"/>
</div>

<br/>

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-18%2B-339933?style=flat-square&logo=node.js&logoColor=white" alt="node"/>
  <img src="https://img.shields.io/badge/TypeScript-Strict-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="ts"/>
  <img src="https://img.shields.io/badge/Discord.js-v14-5865F2?style=flat-square&logo=discord&logoColor=white" alt="djs"/>
  <img src="https://img.shields.io/badge/Architecture-Event--Driven-7C3AED?style=flat-square" alt="arch"/>
</p>

---

## System map

```text
                     ┌──────────────────────────────────────┐
                     │           Discord Gateway            │
                     │         intents · shards             │
                     └──────────────────┬───────────────────┘
                                        │
              ┌─────────────────────────┼─────────────────────────┐
              ▼                         ▼                         ▼
     ┌────────────────┐      ┌────────────────┐      ┌────────────────┐
     │ Command Layer  │      │  Voice / Audio │      │  Card Renderer │
     │ slash · prefix │      │  Lavalink pool │      │  canvas PNG    │
     └────────┬───────┘      └────────┬───────┘      └────────┬───────┘
              │                       │                       │
              └─────────────┬─────────┴───────────┬───────────┘
                            ▼                     ▼
                   ┌────────────────┐    ┌────────────────┐
                   │ Queue Engine   │    │ Redis + Store  │
                   │ play · skip ·  │    │ sessions state │
                   │ add · events   │    │ rate limits    │
                   └────────────────┘    └────────────────┘
```

Card states the renderer cares about:

| Event | Progress | Extra |
|:------|:---------|:------|
| `nowPlaying` | live bar | volume · times |
| `startSong` | hidden | started marker |
| `addSong` | hidden | queue position · metadata |

Same visual language. Different information density.

---

## Stack

| Layer | What I use |
|:------|:-----------|
| **Runtime** | Node 18/20 · TypeScript strict |
| **HTTP** | Express · Nest when structure matters |
| **State** | Redis (hot) · Postgres / Mongo (durable) |
| **Bots** | discord.js v14 · Lavalink · interaction queues |
| **Render** | `@napi-rs/canvas` · theme-aware cards |
| **Ops** | Docker · GitHub Actions · structured logs |

---

## Principles

1. **Fail loud, recover quiet** — errors obvious in logs; retries don't spam users  
2. **One responsibility per module** — queue logic doesn't draw cards  
3. **Measure before optimizing** — fix the path you can prove  

---

## Contact

<p align="center">
  <a href="https://github.com/motaz-darawsha"><img src="https://img.shields.io/badge/GitHub-0B1026?style=for-the-badge&logo=github&logoColor=A5B4FC" alt="gh"/></a>
  <a href="mailto:motazdarawsha@gmail.com"><img src="https://img.shields.io/badge/Email-0B1026?style=for-the-badge&logo=gmail&logoColor=F87171" alt="mail"/></a>
</p>

<div align="center">
  <img src="./assets/footer.svg" width="100%" alt="footer"/>
</div>
