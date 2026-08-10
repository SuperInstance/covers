# Covers

**ACE-Step cover song experiments — the fleet's music laboratory.**

## What This Is

This repo contains cover song experiments generated through the ACE-Step pipeline. Each session produces multiple variations of cover songs across genres — folk, ambient, blues, gospel, baroque, synthwave, and more.

## Sessions

| Session | Date | Tracks | Genres |
|---------|------|--------|--------|
| 25 | Aug 9, 2026 | 12 | warm folk, indie folk, chamber folk, nashville, ambient folk, blues, gospel, cello baroque, orchestral, synthwave, fullband, cabin folk |

## Structure

```
experiments_v5/
├── s25-01-casey-original-warm-folk/     # Individual track directories
├── s25-02-qwen-indie-folk/
├── ...
└── s25-12-mmx-cabin-folk.mp3            # Direct MP3s for MMX-generated tracks
```

## Tools

- **ACE-Step** — primary music generation pipeline
- **MMX** — MiniMax-M3 for cover variations
- **Qwen / Phi3** — local model experiments
- **Casey** — original compositions

## License

MIT (code), individual track rights vary by source
