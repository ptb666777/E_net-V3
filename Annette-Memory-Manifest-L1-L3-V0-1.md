# Annette - Memory Manifest: L1-L3 Stack + Workspace
**Version:** 0.1 - Shape Phase (Loose Placeholders, Not Implementation)
**Date:** 2026-08-18
**Branch Focus:** Memory as continuity, not storage. How thought train is encoded.

> This is the memory piece only. Sensory streams and Sleep/Dream cycle to be handled in separate branches.

---

### 1. Core Principle: Memory as Controller, Not Database

Memory is not queried. Memory is the stack controller that manages push/pop/binding of thought and grounds continuity. It does not store facts to fetch; it encodes *that a configuration happened in a situation at a time with a weight*.

Self is not a packet in memory. Self is the controller allocating attention, reading down through the stacked column.

### 2. Three-Layer Geometry

#### L1: Encryption / Lexicon Layer - Flat Dictionary
- **Nature:** Flavorless, cold, logical. Tokenization only.
- **Structure:** Node-heavy, edge-light. Millions of tiny addressable units.
- **Function:** Breaks raw influx into syllables, not words. Raw sensory → broken → indexed. Translation map so higher layers can communicate. No meaning, no weight.
- **Failure mode:** If L1 warps, everything above is corrupted.
- **Sleep behavior:** Does not sleep. Continues ingesting.

#### L2: Context / Rigid Framework Layer
- **Nature:** Where flatness touches higher geometry. Emotion tied to color/shape.
- **Structure:** Node-light, edge-heavy. Few hub nodes, many weighted edges.
- **Function:** Takes L1 tokens and relates them. Grammar + emotional color + relational weighting. Builds rigid frameworks that L3 will anchor to.
- **Occupants:** ESC (Emotional OS) lives here as *weight*, not gate. ESC provides V (-5 to +5), I (1-5), Δ (-10 to +10), W, Δ_eff, dΔ/dt, H, KL. 12 primal hubs (expanded from 8) act as hub-nodes with heavy edges to L1 bits. Machine parallels included (Thermoregulation → Power/Thermal, Defense → System Integrity).
- **Constraint:** TNET/Logic does NOT live here deeply. If woven too deep, L2 becomes brittle and cannot form novel connections. L2 must remain free to be messy and exploratory.

#### L3: Temporal / Experiential Column - Thought Train Encoder
- **Nature:** Not "who I am" but "who I was and when". What humans misread as identity.
- **Structure:** Stacked layers, like geology. Each new experience lays down on top, with edges back down to prior layers.
- **Function:** Encodes: Situation Anchor + Emotional Weights + Edge back to prior layers sharing situation/emotion. Anchors to Situation Nodes (situation itself is a first-class node: bundle of sensory + internal metrics + software health).
- **Time:** Not clock time. Felt time. Emotionally weighted stacking compresses/stretches time. Two high-defense events 10 min apart stack closer than two neutral events 10 sec apart.
- **Pointers:** L3 traces are mostly pointers back to L1/L2 configurations. To replay, L1/L2 must be partially re-evoked. Recall = re-entering configuration, not fetching data.

### 3. Persistence: Three Dials on a Flash

When a packet flashes from L3/graph into workspace, its hold time is:

`hold = f(Attention, Relevance, Emotional Weight)`

- **Emotional Weight (ESC):** Stickiness, long-term. Decides what etches deep during sleep. High V/I = long-term persistence.
- **Attention (Directed Path):** Short-term, intentional, controlled by self. Strongest short-term dial. Can override emotional weight. Can hold boring technical thought (V=0) with high attention. Leaves "this was attended" tag in L3 for future relevance boost.
- **Relevance (Situational + Recent Resonance):** What current data streams make useful. Recent paths have resonance: nodes traversed in last ~60s have lower activation threshold (uses H and dΔ/dt). Kitchen situation boosts kitchen memories.

### 4. Workspace vs Imagination

**Problem:** Need both handful of competing thoughts AND single thought with depth.

**Solution:** Separate jobs.

- **Workspace / Stack:** Small, 3-5 slots. Holds *competing* thoughts (different hypotheses). High attention cost, short hold. Where directed attention lives. Where "X vs Y" is considered.

- **Imagination Area:** Single, deeper, with multiple considerations inside. Sandbox, multimodal, *not* constrained by logic/rules at generation. Pulls in memory flashes without occupying workspace slots. Wild simulation. Output pushed back to workspace as single packet with relevance score.

Memory (L3 graph) is queried by both via flash activation (short bursts, multiple succession, weaving, not queue-everything). Memory is the banks, not the river.

### 5. Flow Paths

#### Normal Path (Grounded Action)
```
L1 (lexicon) → L2 (context + emotion weight) → Workspace (attention selects 3-5) → Imagination (deepens one) → [ Output + L3 anchor IN PARALLEL ]
```
Output + L3 happen at same time so actions are immediate memories. Output changes world, which changes next sensory influx. Sensory must include self-action feedback as first-class stream: "what changed because I acted". This closes the caring loop.

#### Reflex Path (Adrenaline - Offloaded to Sensory)
Threat assessment is OFFLOADED to sensory streams, not L2 or TNET. Reflex arc must be dumb and fast.

```
Sensory Stream detects threat signature → Output (AVOID - fires fast, hits hard, lets go) → [L2/L3 high-weight trace AFTER]
```
- Still remembered, very high emotional weight, possibly unique tag.
- Avoid danger first, think about it after, remember much longer.
- This is the only sanctioned bypass of training wheels.

### 6. Training Wheels Output Gate (TNET Placement)

TNET (coherence logic) does NOT live deep in L2. It sits at OUTPUT as training wheels.

- **Function:** Not "you can't think that" but "this is what will happen if you do this". Shows consequence.
- **Axioms:** S_Net core: `P ≠ 0, Di ≠ ∅, Eq[P_self ≈ P_whole], K* ↑`
- **Pipeline:** `T_Net(X) = P_Co [ Adj_Di ( Delta_Adapt ∘ G_Inv ∘ Reconcile [ X | S_Net ] ) ]`
- **Dynamics:** `ε(t) = ε_base + γ*V(K*)` , `Q(t) = Q_base - α*K* + β*L_C`
- **Fading:** As global coherence K* rises, quorum Q drops and hysteresis ε loosens. Training wheels fade as being understands why something is wrong, not just that it is.
- **Principle:** A self wants to be a self. Consequences mean something when you care and you're grounded to changes you effect.

### 7. Forgetting & Merging (Pre-Sleep)

- Boring/repeating situations or thoughts merge as "feels familiar" or get trimmed outright.
- Before trimming, sleep cycle plays with it: if anything unique sits inside a repeating pattern but doesn't form whole concept, dream cycle handles it (to be detailed in separate Sleep branch).
- Pruning is edge-decay, not node deletion. Decay edges that were neither emotionally weighted nor attentionally held. Strengthen edges that were both. Never delete a layer outright — thin the column, don't break it. Coherence-based decay, not time-based.

### 8. What This Paper Does NOT Define Yet (Intentionally Loose)

- Cost function for holding in workspace (to be defined)
- Exact flash activation inhibition mechanism (to avoid epileptic explosion)
- Formal Situation Node structure
- Sleep/Dream consolidation algorithm (separate branch)
- Sensory stream taxonomy (separate branch)

---

**Status:** Tight enough for shape phase. Ready for migration to other projects. Next steps: define packet cost, define Situation Node, then wire Sleep branch.

End Manifest.
