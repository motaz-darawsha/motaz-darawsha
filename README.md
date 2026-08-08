<!-- profile: advanced layout -->
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=cy&color=0:0B1026,30:1B1F3B,70:2E1065,100:0B1026&height=220&section=header&text=MOTAZ%20DARAWSHA&fontSize=46&fontColor=E0E7FF&fontAlignY=42&desc=Backend%20Systems%20%E2%80%A2%20Discord%20Infrastructure%20%E2%80%A2%20TypeScript&descSize=14&descAlignY=62&descColor=A5B4FC" width="100%" alt="header"/>
</div>

<br/>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=20&duration=3200&pause=900&color=818CF8&center=true&vCenter=true&width=620&height=55&lines=Event-driven+backends;Music+bots+that+survive+peak+hours;Clean+modules+%C2%B7+explicit+failures" alt="typing"/>
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

Three card states the renderer cares about:

| Event | Progress | Extra surface |
|:------|:---------|:--------------|
| `nowPlaying` | live bar | volume · times |
| `startSong` | hidden | started marker |
| `addSong` | hidden | queue position · metadata |

Same visual language. Different information density.

---

## Stack depth

<div align="center">
  <img src="https://skillicons.dev/icons?i=nodejs,ts,js,express,nestjs,mongodb,postgres,redis,docker,linux,git,github,discord,postman,prometheus" alt="skills"/>
</div>

<br/>

| Layer | What I actually use |
|:------|:--------------------|
| **Runtime** | Node 18/20, TypeScript strict, ESM + CJS bridges when needed |
| **HTTP** | Express for speed, Nest when structure matters |
| **State** | Redis for hot paths, Postgres/Mongo for durable data |
| **Bots** | discord.js v14, Lavalink, interaction queues |
| **Render** | `@napi-rs/canvas`, theme-aware card pipelines |
| **Ops** | Docker, GitHub Actions, structured logs, health checks |

---

## Principles

1. **Fail loud, recover quiet** — errors should be obvious in logs, retries shouldn't spam users  
2. **One responsibility per module** — queue logic doesn't draw cards; cards don't talk to Discord  
3. **Measure before optimizing** — fix the hot path you can prove, not the one you fear  

---

## Contact

<p align="center">
  <a href="https://github.com/motaz-darawsha"><img src="https://img.shields.io/badge/GitHub-0B1026?style=for-the-badge&logo=github&logoColor=A5B4FC" alt="gh"/></a>
  <a href="mailto:motazdarawsha@gmail.com"><img src="https://img.shields.io/badge/Email-0B1026?style=for-the-badge&logo=gmail&logoColor=F87171" alt="mail"/></a>
</p>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0B1026,50:1B1F3B,100:2E1065&height=120&section=footer&text=ship%20small%20%C2%B7%20observe%20hard%20%C2%B7%20iterate&fontSize=14&fontColor=94A3B8&fontAlignY=70" width="100%" alt="footer"/>
</div>
