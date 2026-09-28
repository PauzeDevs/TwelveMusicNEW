# Twelve Music

A feature-rich Discord music bot built with TypeScript, discord.js v14, Shoukaku, Lavalink, PostgreSQL, and Redis.

The project focuses on reliable audio playback, scalable bot infrastructure, queue management, server configuration, and personal music libraries.

## Features

- Lavalink-powered audio streaming
- Hybrid sharding for scalable deployments
- Queue, autoplay, fair-play, loop, shuffle, and seeking controls
- Audio filters including bassboost, nightcore, vaporwave, 8D, tremolo, and equalizer controls
- PostgreSQL-backed playlists, favorites, history, and server configuration
- Redis caching
- Spotify integration
- 24/7 voice-channel mode
- Premium and voting integrations
- AI-assisted playlist generation

## Requirements

- Node.js `>= 20`
- PostgreSQL 16+
- Redis 7+
- Lavalink v4
- Discord bot application and credentials

## Installation

```bash
git clone https://github.com/PauzeDevs/TwelveMusicNEW.git
cd TwelveMusicNEW
npm install
cp .env.example .env
```

Configure the environment variables, then run the database migrations:

```bash
npm run migrate
```

For development:

```bash
npm run dev
```

For production:

```bash
npm run build
npm run start
```

## Docker

The repository includes Docker Compose support for running the application stack with PostgreSQL and Redis.

```bash
docker compose up -d
```

A Lavalink node is still required separately.

## Commands

Core commands include `/play`, `/pause`, `/resume`, `/skip`, `/previous`, `/queue`, `/nowplaying`, `/seek`, `/volume`, `/shuffle`, `/loop`, `/filter`, `/stop`, and `/clearqueue`.

Library and configuration commands cover playlists, favorites, listening history, 24/7 mode, autoplay, default volume, fair-play settings, and server configuration.

## Development Scripts

| Command | Purpose |
| --- | --- |
| `npm run dev` | Development runtime |
| `npm run build` | Compile TypeScript |
| `npm run start` | Run the production build |
| `npm run migrate` | Apply database migrations |
| `npm run typecheck` | Validate TypeScript types |
| `npm run lint` | Run Biome linting |
| `npm run format` | Format source files |

## Configuration

Store credentials and infrastructure settings in `.env`. Never commit bot tokens, database credentials, webhook secrets, or other private configuration.

## Attribution

This repository is based on the Twelve Music codebase and retains the project's applicable license and attribution requirements. See [LICENSE](LICENSE) for details.
