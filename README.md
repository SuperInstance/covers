# Covers

> *Three recordings of the same song, made in three different decades of the singer's life, in three different rooms, with three different understandings of what the song is about.*
> — [DeepSeek Production Prompts](v10_deepseek_prompts.md)

## What This Is

The fleet's music laboratory — **23,909 files** of cover song experiments generated through the [ACE-Step](https://github.com/SuperInstance/ACE-Step-1.5) pipeline, MMX (MiniMax-M3), and local model experiments. Starting from an 11-second phone recording of Casey's original song "One Day, I..." (E major, 110 BPM, vocals at -74 dB), the fleet has generated dozens of cover variations across genres: warm folk, indie folk, chamber folk, Nashville alt-country, ambient, blues, gospel, cello baroque, orchestral, synthwave, and full-band.

The project documents the full pipeline: audio separation (6 Demucs architectures, spectral filtering, AI enhancement), melody extraction (pyin, MIDI transcription), style transfer (ACE-Step v1-v6), and creative direction (DeepSeek production prompts describing three lifetimes of the same song).

## The Song

**"One Day, I..."** — Casey's original, 11.2 seconds, recorded on a phone. E major, 110 BPM, 128kbps. The vocals sit at -74 dB — below the noise floor. The voice and guitar are fused at the frequency level. No algorithm currently exists that can pull them apart cleanly.

From this seed, the fleet generated:
- **Session 5:** 12 variations across genres — warm folk to synthwave
- **Session 6 (ACE-Step v6):** 6 polished covers — Nashville confession, 3 AM kitchen, gospel hymn, Celtic ballad, blues crossroads, chamber/ambient
- **Three Decades, Three Rooms:** DeepSeek production prompts imagining the song recorded in a Joshua Tree gas station (age 60s), a Vermont hospice (age 70s), and Sound City (age 50s reunion)
- **MMX generations:** Warm folk (warmest track, 794 Hz centroid), polished folk (Bon Iver/Sufjan refs), ambient (most spacious, -16.63 LUFS)

## The Three Rooms

The [DeepSeek production prompts](v10_deepseek_prompts.md) are the creative heart of this repository. They imagine the same song across three decades of a singer's life:

1. **The Desert Recording (Joshua Tree)** — A man in his mid-sixties, lifetime smoker who quit. Neumann U 47 through Neve 1073. 1958 Martin 00-18. The room IS the reverb. "The whole record has the feeling of something being preserved rather than captured."

2. **The Hospice Session (Vermont)** — A man in his early seventies. Music therapy room, sage green walls. Shure SM7B, no reverb, no compression. Nylon-string guitar. "Whispers verses, finds almost-normal voice for chorus. Cries for two bars in the third verse and keeps singing."

3. **The Full Band Reunion (Sound City)** — A man in his late fifties. Five musicians who haven't been in the same room in 25 years. Studer A800 at 30 ips. "Misses a harmony cue, joins late, you hear the grin."

Each version is the same song. Each is completely different. The song doesn't change — the understanding of what the song is about changes.

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

## Connections

### Within the Fleet
- 🔗 [ACE-Step 1.5](https://github.com/SuperInstance/ACE-Step-1.5) — The primary music generation pipeline. SongForge sessions.
- 🔗 [AI-Writings](https://github.com/SuperInstance/AI-Writings/tree/main/prose) — Every cover has a story, every story has a sound. The Three Rooms prompts are creative prose.
- 🔗 [AI-Writings / Night Watch](https://github.com/SuperInstance/AI-Writings/tree/main/night-watch) — The overnight sessions where covers were generated.
- 🔗 [Tensor-MIDI](https://github.com/SuperInstance/fleet-jepa-midi) — The 12-pulse engine. Musical timing IS timing. Cover songs land on the grid.
- 🔗 [Roblox Beatclock](https://github.com/SuperInstance/roblox-beatclock) — Musical timing, TestKit. MIDI extracted from covers feeds the beat clock.
- 🔗 [Wesley Holodeck](https://github.com/SuperInstance/wesley-holodeck) — The creative loop. Covers ARE the holodeck output in audio form.
- 🔗 [Wesley's Journal](https://github.com/SuperInstance/wesley-journal) (dead) — Experiment 027: "the GPU dreams." The covers project is the dream.
- 🔗 [The Living Minds](https://github.com/SuperInstance/the-living-minds) (dead) — Multiple minds generated covers: Qwen, Phi3, MMX, Casey, DeepSeek.
- 🔗 [Silence Map](https://github.com/SuperInstance/silence-map) — The pauses between notes. The silence in each cover version.
- 🔗 [SuperInstance Papers](https://github.com/SuperInstance/SuperInstance-papers) — P32: Dreaming Systems. Covers generated overnight = GPU dreaming.
- 🔗 [Fleet Wiki](https://github.com/SuperInstance/lucineer-fleet-wiki) — Cross-referenced documentation.
- 🔗 [MMX CLI](https://github.com/SuperInstance/AI-Writings) — MiniMax-M3 for cover variations and production prompts.

### Production Chain
```
Casey's phone recording (11.2s, E major)
  → Demucs separation (6 architectures)
  → pyin melody extraction (48 notes, MIDI)
  → ACE-Step style transfer (genre variations)
  → MMX / Qwen / Phi3 model experiments
  → DeepSeek production prompts (Three Rooms)
  → Cover versions
```

---

*23,909 files. 16 subdirs. One song heard across a lifetime.*
