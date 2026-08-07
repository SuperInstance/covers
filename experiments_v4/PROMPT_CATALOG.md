# SongForge Prompt Catalog — Session 3 (Prepared)

## For Next MMX Quota Window

These prompts are prepared and ready to fire when the MMX general quota resets. Each explores a fundamentally different musical space for Casey's "Molding Memories."

---

### V4-1: The Weathered Nashville (Alt-Country)
```
Alt-country indie folk in the vein of Jason Isbell's Something More Than Free. 
Worn-in male baritone voice, late twenties timbre with gravel on the edges. 
Pedal steel guitar weaving through fingerpicked acoustic. Brushed snare, 
minimal drumkit. Bass guitar anchoring the low end. The arrangement starts 
sparse — just voice and guitar — and builds gradually as the verses progress. 
Porch music, dusk light, the air heavy with memory. The voice should sound 
like it has lived in these words for years. Warm, intimate production with 
room ambience.
```
- Vocals: "weathered male baritone, Jason Isbell-esque, lived-in and tender"
- BPM: 105, Key: E major

### V4-2: The Chamber Folk (Sufjan Territory)
```
Chamber folk in the style of Sufjan Stevens' Carrie & Lowell. Almost whispered 
male vocals, breathy and fragile, barely above a murmur. Solo fingerpicked 
nylon-string acoustic guitar, so quiet you can hear the fingernails on the 
strings. Occasional piano notes like raindrops. Subtle atmospheric hum, drone 
textures barely perceptible. The production is extremely intimate — recorded 
close, room sound present, like being inside the singer's chest cavity. No 
drums. No bass. Just voice, guitar, and the ghost of a piano. The mood is 
devastating tenderness.
```
- Vocals: "breathy male tenor, half-whispered, fragile, Sufjan Stevens-like"
- BPM: 85, Key: E major

### V4-3: The Gospel-Folk Hymn (Spiritual Arc)
```
Gospel-folk hymn in the spirit of Hozier's acoustic work and The Swell Season. 
Starts with a single unaccompanied male voice — raw, chest-voice, full of 
belief. Acoustic guitar enters fingerpicking a simple pattern. By the first 
chorus, a subtle organ joins. By the second verse, brushed drums and bass. 
By the final chorus, a full choir of voices joins — not polished studio choir 
but rough community-church choir, voices slightly out of unison, clapping on 
the backbeat. The song builds from absolute solitude to a congregation.
```
- Vocals: "soulful male tenor building to full-voice, joined by rough community choir"
- BPM: 100, Key: E major

### V4-4: The Jazz-Folk Kitchen (2 AM Conversation)
```
Late-night jazz-folk crossover. Think Gregory Porter meets Iron & Wine. 
Warm upright bass walking gently under fingerpicked acoustic guitar. Brushed 
jazz drums, very sparse — just texture and color. A vibraphone echoing the 
vocal melody in the spaces between lines. The voice is a rich, smooth male 
baritone with just enough roughness to sound honest. Piano comping softly 
in the middle distance. Space is the most important instrument.
```
- Vocals: "rich warm male baritone, Gregory Porter-style phrasing"
- BPM: 90, Key: E major

### V4-5: The Older Voice Cover (Cover Mode on generate_polished.mp3)
```
Stripped-down acoustic folk, a single weathered older male voice, fingerpicked 
guitar. The voice should be lower, rougher, more lived-in than the original. 
Think an older man hearing his young self on tape. Intimate, close-mic, no 
reverb.
```
- Source audio: generate_polished.mp3 (studio quality, should pass DTW)

### V4-6: The Fingerstyle Virtuoso (Tommy Emmanuel Territory)
```
Fingerstyle acoustic guitar instrumental with subtle humming/vocalizations. 
Think Tommy Emmanuel or Andy McKee playing a reflective piece. The guitar 
carries the entire melody — bass notes walking under treble arpeggios, 
harmonics ringing like bells, percussion on the guitar body. If vocals 
appear, they are barely-there hummed fragments, not full lyrics. The 
technical skill is high but the emotion is higher. This is what the song 
sounds like when only the guitar remembers it.
```
- Vocals: "subtle male humming, barely audible, ghost-voice"
- BPM: 95, Key: E major

### V4-7: The Lo-Fi Bedroom (Elliott Smith Four-Track)
```
Lo-fi bedroom folk recorded on a four-track cassette. Think Elliott Smith's 
early solo work or early Bon Iver. Thin, double-tracked vocals panned hard 
left and right, slightly out of sync. Acoustic guitar recorded too hot, 
slight distortion on the transients. Hiss and hum from the tape. The sound 
of someone alone in a room at 3 AM, working out their feelings onto magnetic 
tape. The vulnerability is in the imperfections.
```
- Vocals: "thin double-tracked male tenor, intimate, Elliott Smith-style"
- BPM: 88, Key: E major

### V4-8: The Celtic Ballad (Planxty / Sinead O'Connor)
```
Celtic-tinged folk ballad. Think Planxty's acoustic intimacy meets Sinead 
O'Connor's emotional directness. Acoustic guitar in dropped-D tuning, 
uilleann pipes entering on the second verse, bodhrán frame drum 
underscoring the chorus. The voice is clear and unadorned — a pure tenor 
with a slight Irish lilt on the vowels. The song sounds centuries old, 
like it was passed down through generations. The arrangement is sparse — 
each instrument enters only when it has something to say.
```
- Vocals: "clear male tenor with slight Irish inflection, pure and unadorned"
- BPM: 82, Key: E major

---

## Suno API Pipeline (Alternative Platform)

The Suno upload-and-extend API offers a fundamentally different approach:

1. **Upload** Casey's original 11.2-second recording to Suno
2. **Extend** it with a style prompt — Suno continues the song from where it stops
3. This preserves the original 11 seconds AS-IS and generates new material around/after it

This is the closest to a true "cover" because the original recording is 
preserved within the output. The API endpoint is:
```
POST https://api.sunoapi.org/api/v1/generate/upload-extend
```

Required: SunoAPI credits (~$5 for 1000 credits, upload-extend costs ~12 credits)

## RVC Two-Stage Pipeline (Voice Conversion)

For true voice conversion (preserving melody, changing voice):

1. Generate a clean vocal performance with MMX (already done)
2. Separate vocals from the generated track (Demucs — already set up)
3. Run the isolated vocals through RVC with a "weathered older male" voice model
4. Mix the RVC-converted vocals back with the instrumental
5. This preserves the song's melody exactly while transforming only the vocal character

RVC can run on Google Colab (free GPU) with pre-trained voice models.
