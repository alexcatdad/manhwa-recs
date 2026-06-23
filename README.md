# Manhwa Recs

Open-source private reading tracker and recommendation backlog for manhwa, webtoons, manga, and adjacent serial fiction.

The app is intentionally scoped around structured reading state and reviews, not a chat interface and not content scraping.

## Product Direction

- Convex app for database, auth, API functions, scheduled jobs, and external calls.
- Private deployment data by default.
- Open-source codebase with no private user data committed.
- Title search, list management, review capture, and background enrichment.
- Official platform links, such as Tapas, WEBTOON, Manta, Tappytoon, and publisher/creator sites.
- Batched LLM calls through OpenRouter for claim extraction, taste-profile aggregation, and recommendation generation.

## Non-Goals

- No image hosting or chapter reader.
- No chapter text ingestion.
- No scraping licensed content.
- No chat interface in the MVP.
- No public/shared data corpus until private single-user or small-group flows work.

## Core User Flow

1. Search for a title.
2. Add it to a personal list.
3. Mark status: want to read, reading, up to date, read, stalled, or dropped.
4. Write a review or notes.
5. Background jobs enrich metadata and extract preference claims.
6. Recommendations are generated from structured status, reviews, tags, and source-backed metadata.

## Data Sources

The app should prefer durable, auditable sources:

- First-party user reviews and status.
- Friend or private group submissions.
- Official platform links.
- Metadata APIs such as AniList, Kitsu, Wikidata, and carefully scoped MangaDex/MangaUpdates-style metadata.

Every imported source should keep provenance, timestamp, confidence, and refresh status.
