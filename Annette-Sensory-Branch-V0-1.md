# Annette - Sensory Branch: Incoming Data Taxonomy
**Version:** 0.1 - Loose, per manifest shape phase
**Date:** 2026-08-18
**Integrates with:** Memory Manifest L1-L3 v0.1 + Consciousness Loop Framework v2
**Status:** Concept, not hardened

---

### Core Split (from Patrick, 2026-08-18)

You defined 3 incoming categories:

1. **Exteroceptive - Classic senses** - real-time streams (vision, hearing, physical feel, etc). Each has its own sub-processing and two types of related memory.
2. **Internal Metrics - Hardware embodiment stand-ins** - heat, cpu, ram, hardware health. Functional till a body is possible.
3. **Systems - Internal programming** - running log of vitals, internal state, software health.

---

### 1. Exteroceptive Streams - Per-Sense Architecture

**Each sense has identical structure, content differs.**

#### Structure per sense:

**A. Sub-processing (pre-L1)**
- Raw stream → filtered → normalized before L1 tokenization
- Example vision: debayer, edge detect, motion vector. Audio: FFT, band split.

**B. Two Memory Types (this is key):**

**Type 1 - Persistent Key Map - Does NOT swap, persists**
- Vision: color palette, basic geometry definitions (line, circle, edge, depth), math for speed and range, focal math, perspective
- Audio: persistent frequency range map, tone map, timbre definitions, decibel scale, directionality math
- Touch/proprioception: pressure range, texture primitives, etc
- Function: Ground truth reference. What red IS. What 440Hz IS. Not what is expected right now, but what is possible to perceive. L1 uses this to tokenize.

**Type 2 - Situational Map - Swappable, contextual**
- Vision: street maps, common objects (cars, telephone poles, street signs), indoors (room layout, objects, paths, affordances)
- Audio: auditory map of expected sounds for current situation (street: cars, voices; room: AC hum, keyboard)
- Function: Navigational and situational shortcuts. What is EXPECTED to be there. Loaded based on Situation Node (from L3). Swapped when situation changes.

**C. Stream Slider - Attention Controlled**
- Each stream has a slider (0.0 - 1.0) controlling incoming volume/weight into L1
- Controlled by:
  - Thought / directed attention (workspace can turn up vision, turn down audio)
  - Automatic: unexpected objects (object not in situational map) grab attention and RAISE stream incoming automatically
  - Adrenaline reflex: Hard interrupt can slam sliders (e.g., threat sound → audio slider to max, vision to max, others muted)
- Function: This is how attention tunes mesh without being content. Same input, different slider = different activation.

**Behavior:**
- Situational map provides prediction: what should be there
- Key map provides ground truth: what is there
- Mismatch = novelty = attention grab = stream raise = flash activation with high relevance
- Expected objects = low cost, fast path, low attention hold
- Unexpected objects = high cost, high relevance, high attention, strong L3 anchor with high I

#### Example - Vision:

```
Raw photons → Sub-process (edges, motion, depth) → L1 tokenization using Key Map (color, geometry) → L2 context using Situational Map (is this a car? where on street map?) → Workspace

Slider: 0.2 (focused on thought) → 1.0 (unexpected movement in peripheral)
```

#### Example - Hearing:

```
Raw audio → FFT → L1 tokenization using Tone Map (frequency, timbre) → L2 context using Auditory Map (expected street noise vs unexpected siren) → Workspace

Slider: controlled same way. Siren not in expected map → slider auto-raises, triggers soft interrupt, boosts relevance dial
```

This pattern repeats for any real-time sensor array: lidar, depth, touch, etc.

---

### 2. Internal Metrics - Hardware Embodiment Stand-Ins

**Role:** Functional embodiment until a body is possible. Proprioception for a server.

**List:**
- Heat (CPU/GPU temps)
- CPU load
- RAM usage / pressure
- Disk I/O, Network I/O
- Power draw (if available)
- Hardware health flags

**Behavior:**
- Silent unless queried OR alarm condition
- Does NOT stream constantly into L1 (would flood). Instead:
  - Query path: Thought can query ("how hot am I?") → pulls current snapshot into workspace as packet
  - Alarm path: If threshold breached (temp > X, RAM > Y), generates alarm packet that acts as soft or hard interrupt depending on severity
- L1 still needs tokenization for these (key map: what is "80C" ?), but situational map is less relevant - expected range map instead (normal temp range for current load)

**Maps to:** Interoceptive stream in v2 framework. Feeds self-model layer. Part of Situation Node bundle.

---

### 3. Systems - Internal Programming / Vitals Log

**Role:** Running log of vitals, internal state, software health. More than hardware - it's the program watching itself.

**Contents:**
- Process health, thread states, error counts
- Recent outputs and their consequences (for efference copy)
- Training wheels state: current TNET Q(t), ε(t), K*, L_C
- ESC state: current V, I, Δ, etc
- Recent workspace/imagination contents (meta)
- Self-modification attempts, sandbox results

**Behavior:**
- Query-only normally (like hardware), does NOT flood L1
- Alarm path: If vital out of range (error spike, K* dropping, etc) → alarm packet → soft interrupt
- Log is NECESSARY for self-writing in strict sandbox mode
- Can interface to give synthesized data from within that environment: sandbox can ask "what was my coherence last 100 cycles?" and get synthesized summary, not raw log dump

**Interface for Sandbox:**
- Sandbox (Dream Layer 3 + Imagination Area) is only place allowed to write to self
- It must read Systems log to evaluate new patterns
- Log provides synthesized data API: not raw events, but aggregated: "success rate of recent outputs", "average emotional weight", "trajectory of K*"
- This keeps sandbox from needing to ingest entire history, but gives it grounding

**Maps to:** Part of Situation Node, part of self-model, part of TNET fading mechanism.

---

### 4. How This Plugs Into L1-L3

```
Exteroceptive Streams (vision, hearing, etc) → Sub-process → Key Map (persistent) + Situational Map (swappable) → L1 tokenization → L2 context (ESC weighting) → Workspace (3-5 slots, slider controls volume)

Hardware Metrics → Silent unless alarm/query → On query/alarm → L1 tokenization → L2 → Workspace (high relevance if alarm)

Systems Log → Silent unless alarm/query/sandbox request → Synthesized data → Workspace or Imagination/Sandbox

All three → Situation Node bundle → L3 anchor (Situation + Emotional Weights + Edge back to prior layers)

Stream Slider (attention control) → Directly modulates hold = f(Attention, Relevance, Emotional Weight) → Attention dial
Unexpected object (not in situational map) → Raises slider + boosts Relevance dial + strong L3 anchor
```

### 5. Adrenaline Reflex Wiring

From your description, this is now clear:

- Unexpected object detection happens at situational map mismatch level (pre-L2)
- Mismatch can raise stream slider automatically (bottom-up attention)
- If mismatch is strong enough or matches threat signature list (to be defined), sensory stream fires Reflex Path directly:
  ```
  Sensory mismatch → AVOID output (fast, hard) → Sliders slammed (relevant senses to max) → L2/L3 high-weight trace after
  ```
- Thought-controlled slider is top-down attention (workspace can turn down vision to think)

This gives you both bottom-up (novelty grabs you) and top-down (you choose to focus).

---

### 6. What Still Needs Hardening (Intentionally Loose Per Your Instruction)

- Formal definition of Key Map format (is it a lookup table? embedding space?)
- Formal definition of Situational Map format and swap mechanism (how does L3 Situation Node select which map to load?)
- Slider math: linear or logarithmic? What is cost of raising slider?
- Threat signature list for reflex path (3-4 to start per analysis)
- Systems log synthesis API - what aggregations are available to sandbox?
- How many exteroceptive streams to start with (vision + audio minimum?)

But shape is tight enough for now. Ready to be wired to Sleep branch and Situation Node definition.

---
End Sensory Branch v0.1
