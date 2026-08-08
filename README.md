<div align="center">
  <img src="./assets/header.svg" alt="Motaz Darawsha" width="100%"/>
</div>

<br/>

<div align="center">
  <img src="./assets/status.svg" alt="status" width="100%"/>
</div>

<br/>

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-18%2B-339933?style=flat-square&logo=node.js&logoColor=white"/>
  <img src="https://img.shields.io/badge/TypeScript-Strict-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/Discord.js-v14-5865F2?style=flat-square&logo=discord&logoColor=white"/>
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
</p>

---

### System

```text
Discord Gateway
      │
      ├── Commands ──▶ Queue Engine ──▶ Voice / Lavalink
      │
      └── Card Renderer  (nowPlaying · startSong · addSong)
               │
               └── Redis / DB  (session · rate limits)
```

| Event | Bar | Shows |
|-------|-----|--------|
| `nowPlaying` | on | time + volume |
| `startSong` | off | started state |
| `addSong` | off | queue position |

---

### Stack

**Runtime** — Node 18/20, TypeScript  
**Bots** — discord.js v14, Lavalink  
**Data** — Redis, MongoDB / PostgreSQL  
**Render** — `@napi-rs/canvas`  
**Ops** — Docker, GitHub Actions  

---

### Contact

<p align="center">
  <a href="https://github.com/motaz-darawsha"><img src="https://img.shields.io/badge/GitHub-0B1026?style=for-the-badge&logo=github&logoColor=A5B4FC"/></a>
  <a href="mailto:motazdarawsha@gmail.com"><img src="https://img.shields.io/badge/Email-0B1026?style=for-the-badge&logo=gmail&logoColor=F87171"/></a>
</p>

<div align="center">
  <img src="./assets/footer.svg" alt="footer" width="100%"/>
</div>
