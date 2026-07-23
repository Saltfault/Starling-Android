# Starling Android

Android client for **[Starling](https://forgejo.hearthhome.lol/Saltfault/Starling)** — a federated, peer-to-peer communications platform with no company in the middle.

> **Status: 📋 Planned — not yet started.**
> The terminal client, **[Starling-TUI](https://forgejo.hearthhome.lol/Saltfault/Starling-TUI)**, is the working client today. This repo is a placeholder for the phone app.
> A phone app won't install through the desktop launcher — it'll ship as a normal Android package when ready.

---

## What this will be

Starling in your pocket: join a flock, chat, and take voice/video calls over the murmuration from an Android phone — peer-to-peer, end-to-end encrypted, with no central server routing your messages.

The mobile build has the hardest constraints of any client — background connectivity, battery, doze mode, and OS mic/camera permissions — which is why it comes after the desktop and web clients prove the shared core on easier ground.

## How it's built (planned)

Same stack as the desktop and web clients: a **Solid.JS** frontend in a **Tauri** shell (Tauri targets Android as well as desktop), with the [`starling-server`](https://forgejo.hearthhome.lol/Saltfault/Starling-Server) library as the Rust backend, cross-compiled for `aarch64-linux-android`. Sharing the frontend and core with the other clients is the whole point — the mobile-specific work is in the shell, not the protocol.

| Piece | Stack |
|-------|-------|
| Frontend | Solid.JS |
| App shell | Tauri (Android target) |
| Protocol / networking | [`starling-server`](https://forgejo.hearthhome.lol/Saltfault/Starling-Server) library, cross-compiled for Android |
| Open questions | Background service model, push/wake strategy, foreground-call notifications |

## Following along

- Design and roadmap live in the main **[Starling](https://forgejo.hearthhome.lol/Saltfault/Starling)** repo.
- The protocol this will implement is documented in **[Starling-Server](https://forgejo.hearthhome.lol/Saltfault/Starling-Server)**.

## License

Apache 2.0
