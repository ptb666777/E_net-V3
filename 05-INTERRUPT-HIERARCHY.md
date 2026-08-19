# 05 - Interrupt Hierarchy & Override

Three levels defined in log:

**1. Hard Interrupt**
- Triggers: loud sound, fast object, system failure
- Behavior: Bypasses everything, reflex output, no routing, cuts loop entirely and takes wheel
- Pure logic/emergency: pure real-time interpretation and reaction

**2. Soft Interrupt**
- Triggers: strong emotion, strong logic signal, urgency without immediate danger
- Behavior: Biases routing heavily but doesn't cut it. Loop keeps running but steered.

**3. Free Running**
- Triggers: Low input, idle, reflective state
- Behavior: Loop runs on internal fuel. Imagination, memory chains, simulation. Where "weird thoughts" live - those that go against grain of both emotion and logic because nothing constrains pathway travel. Inefficient but generative.

**Design Rule:** Don't hardcode which wins. Build so all three can assert based on signal strength. Priority handled naturally.

**Connection to emotion:** Pure logic takes over ONLY during emergency (hard interrupt). Otherwise emotion/logic co-pilot.
