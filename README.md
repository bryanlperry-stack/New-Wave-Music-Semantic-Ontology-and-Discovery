# New-Wave-Music-Semantic-Ontology-and-Discovery
A machine-readable SKOS-compliant taxonomy and RDF graph modeling New Wave sub-genres and sonic textures for music recommendation.
## Executive Summary & Problem Statement
### The Domain Problem
Commercial music streaming platforms (e.g., Apple Music, Spotify) rely on collaborative filtering and broad temporal tags. As a result, distinct New Wave artists such as: 
### Joy Division (dark post-punk)
### The Human League (classic synth-pop)
### Gary Numan (dark synth-pop) 
### The Cars (guitar-driven power pop)
### Duran Duran (dance-rock / pop-rock) 
### Ultravox (synth-rock / theatrical-Rock / symphonic art-rock) 
### ABC (synth pop/synthesizer-driven new pop/blue-eyed soul/post disco)
are frequently lumped into a single continuous "1980s New Wave" or "New Wave" playlist. Because New Wave (1977-1984) was a multi-genre, cross-decade music movement, using it as a Broad Term to curate music is far too imprecise for increasingly granular taxonomies of music discovery.
### Discovery Friction
For listeners–particularly younger generations, like Generation Z, exploring historical genres–this creates significant friction. Generation Z often listens to music for sonic textures, sonic vignettes and "vibes", rather than strict genres, so having to skip through songs on a single playlist due to constant genre-switching is a point of frustration. Furthermore, because "New Wave" is used as an overarching Broader Term, and because the label "Synth Pop" is often too liberally applied to artists who diverge greatly from established synth-pop sonic attributes, similar-sounding artists who are not classified as "new wave", but who share sonic similarities with artists featured on New Wave playlists, remain hidden from user discovery 
### Example: (e.g., Duran Duran -> 1980s dance rock/funk rock -> shared sonic similarities -> Prince/Prince and the Revolution, INXS, Rick James, Power Station).
### The Architectural Solution
Because New Wave (1977-1984) was a multi-genre music movement that serves as a temporal layer for music taxonomy and discovery, 

## Taxonomy Hierarchy & Sonic Texture Schema
To resolve flat-genre siloing, this taxonomy decouples temporal anchors from acoustic textures. Below is the multi-dimensional SKOS concept hierarchy modeled in 'vocab/new-wave-taxonomy.ttl":

```text
New Wave & Sonic Texture Taxonomy (SKOS Scheme)
│
├── 1. Temporal Anchor Nodes (Historical Movements)
│   └── New Wave (c. 1977–1984)
│
├── 2. Sonic Texture & Micro-Genre Hierarchies
│   │
│   ├── i.Electronic Music Family (Top Concept)
│   │     ├── Synth-pop (Broader)
│   │     │   ├── Coldwave (Narrower)
│   │     │   ├── Retro Synth-pop
│   │     │   ├── Bubblegum Synth-pop (Narrower)
│   │     │   └── Techno-pop (Narrower)
│   │     │       ├── Neo-Shibuya-kei (Narrower)
│   │     │       ├── Pico-Pico Pop (Narrower)
│   │     │       └── [skos:related] ──> Chiptune
│   │     │    
│   │     ├── Eurodisco (Broader)
│   │     │   └── [skos:Related] Italo Disco / Eurodance / Trance / Eurodance/ House
│   │     │
│   │     └── Italo Disco (Top Concept/Broader)
│   │     │   ├── Spacesynth (Narrower)
│   │     │   ├── Synthwave (Narrower)
│   │     │   ├── Hi-NRG (Narrower)
│   │     │   │   └── [skos:related] ──> Eurodance / House / Synth-pop / Post-Disco
│   │     │   └── [skos:related] ──> Synth-Pop / House / Trance / Techno /Eurodance
│   │     │
│   │     └── Indietronica / Hipster Synth-Pop / Indie Synth-Pop (Narrower/ 2000s-2010s Crossover)
│   │         └── Indie Sleaze (Narrower / Aesthetic Micro-Genre) 
│   │
│   ├── ii.Punk & Post-Punk Family (Top Concept)
│   │      ├── Punk Rock (Broader)
│   │      │   ├── Reggae Punk (Narrower)
│   │      │   ├── Hardcore Punk (Narrower)
│   │      │   └── Ska Punk (Narrower)
│   │      │       └── [skos:related] ──> Two-Tone / Alternative Rock / Reggae Rock
│   │      │      
│   │      └── Post-Punk (Broader)
│   │          ├── Two-Tone (Narrower)
│   │          │   └── [skos:related] ──> Ska Punk 
│   │          ├── Goth Rock (Narrower)
│   │          ├── Industrial Rock (Narrower)
│   │          ├── No Wave (Narrower)
│   │          └── [skos:related] ──> Coldwave / Synth-pop
│   │
│   └──  iii.Rock & Pop Music Family (Top Concept)
│   │        ├── Art Rock (Narrower)
│   │        │   └── Theatrical Rock (Narrower)
│   │        │   └── Synth-Rock (Narrower)
│   │        │   └── [skos:related] ──> New Romanticism / Symphonic Rock / Theatrical Rock / Art Rock
│   │        │
│   │        ├── New Wave Pop (Narrower)
│   │        │   ├── New Pop (Narrower)
│   │        │   │   └── [skos: related] ──> Post-Disco / Synth-Pop / Dance-Rock/ Blue-Eyed Soul / Glam Rock / 
│   │        │   └── Sophisti-Pop (Narrower)
│   │        │       └── [skos: related] ──> Soul / Progressive Pop / Synth-Pop / Adult Contemporary / Blue-Eyed Soul / Smooth Jazz / Jazz                                               Pop / Bossa Nova
│   │        ├── Dance-Rock (Narrower)
│   │        │   └── [skos:related] ──> Funk Rock / Post-Disco / Punk Funk / Minneapolis Sound
│   │        │
│   │        ├── Power Pop (Narrower)
│   │        │   └── [skos:related] ──> Jangle Pop / New Wave / Synth-pop
│   │        │  
│   │        └── Alternative Rock (Narrower)
│                ├── College Rock (Narrower)
│                ├── Jangle Pop (Narrower)
│                └── [skos:related] ──> Post-punk / New Wave / Power Pop / Indie Pop
```

![image](https://github.com/bryanlperry-stack/New-Wave-Music-Semantic-Ontology-and-Discovery/blob/main/Electronic%20Music%20Family.drawio.png)



