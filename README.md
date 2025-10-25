DSPDNA-M

DSPDNA-M (Digital Signal Processing + Musical DNA) is a research framework and AI system designed to decode the complete genetic structure of music — uniting the engineering and compositional layers that define every track.

It reads both the sound design DNA (how the audio was shaped) and the musical DNA (how it was written, arranged, and performed), producing a transparent, structured description of any song.

Overview

DSPDNA-M analyzes finished audio to reconstruct two complementary layers:

Layer	Focus	Output

Engineering DNA (DSP)	EQ, compression, saturation, spatial effects, routing, automation	DAW-agnostic session map (JSON)

Musical DNA (Theory)	Chords, key, melody, rhythm, motifs, song form	Symbolic music map (key, phrases, progressions)

These layers combine into a unified audio genome — a representation of both how a song sounds and what it expresses.

Core Architecture

Component	Description
Decoder	Interprets a mixed audio file to infer both DSP and music-theory structures.

Supervisor	Trains and refines the Decoder using paired DAW session exports and symbolic annotations.
Ontology	Canonical vocabulary of DSP devices, parameters, and musical objects (EQ, compressor, chord, motif, etc.).

Cookbook	Genre- and instrument-based priors describing typical production and harmonic patterns.
Plugin Zoo	Library of learned plugin “fingerprints” for probabilistic plugin and preset equivalence.

Music Analyzer	Symbolic engine that performs chord, melody, rhythm, and form extraction.


⸻

Example Output

{
  "track": "LeadVox",
  "music_analysis": {
    "key": "C major",
    "tempo_bpm": 120,
    "section": "chorus",
    "chord_progression": ["C", "G", "Am", "F"],
    "melodic_role": "lead",
    "motif": "stepwise-up",
    "phrase_length_bars": 8
  },
  "dsp_chain": [
    {"class": "eq_parametric", "params": {"f_hz": 3200, "gain_db": 2.5, "q": 1.1}},
    {"class": "compressor_fet_fast", "params": {"threshold_db": -17, "ratio": 4.0}},
    {"class": "reverb_plate", "params": {"rt60_s": 1.3, "mix_percent": 22}}
  ],
  "confidence": 0.89
}


⸻

Research Goals
	•	Develop a bi-layered model that understands both acoustic engineering and compositional structure.
	•	Create an open, DAW-agnostic ontology for describing sessions and music theory in machine-readable form.
	•	Enable forensic, educational, and creative applications — from mix deconstruction to assisted learning.
	•	Progress toward an audio genome: a comprehensive representation of every track’s physical and musical DNA.
  
Repository Structure

DSPDNA-M/
 ├── docs/               # Technical notes, architecture, ontology references
 ├── schema/             # JSON Schema for DSP + music maps
 ├── data/
 │    ├── plugin_zoo/    # Plugin and preset fingerprints
 │    ├── cookbook/      # Genre and instrument priors
 │    └── stems/         # Example training stems
 ├── models/
 │    ├── decoder_core.py
 │    ├── supervisor.py
 │    └── music_analyzer.py
 ├── train/
 │    ├── train_decoder.py
 │    ├── train_supervisor.py
 │    └── evaluate.py
 ├── examples/
 │    └── SessionMap_example.json
 ├── README.md
 └── LICENSE


License

Released under the Apache License 2.0 free for research and open development with explicit patent protection.
See LICENSE for details.

Project Vision

Every song has DNA. DSPDNA-M is teaching AI to read it both in the mix and in the music.
