# Tumtum's Maelstrom Weaver

This is a WeakAuras package for WotLK (3.3.5a client) enhancement shaman spell-weaving. It overlays main-hand/off-hand swing timing, spell cast thresholds, sync state, latency-adjusted safe windows, and optional maelstrom/gcd helpers.

## Features

- Main-hand swing timer with safe weave window
- Off-hand “too early” threshold
- Lightning bolt and chain lightning cast thresholds
- Latency-adjusted spell ticks
- Chain lightning/lightning bolt safe-window coloring
  - Green = chain lightning available
  - Blue = lightning bolt fallback
- Main-hand/off-hand sync detection
- Melee-context gating to suppress fake ranged-cast swing cycles
- Optional gcd overlay
- Optional maelstrom tracker
- Optional 5-stack maelstrom glow for the maelstrom tracker
- Optional debug text

## Install

1. Download or open `maelstrom-weaver.txt`
2. Copy the entire export string
3. In-game, open `/wa`
4. Click `import`
5. Paste the string
6. Accept/import

## Configuration

Open the weak aura group and adjust options in the settings/controller aura.

Recommended defaults:

- Sync threshold: `0.50s`
- Show both spell ticks: off
- GCD overlay: off
- Maelstrom tracker: on
- 5-stack maelstrom glow: off

### Sync Threshold

Default: `0.50s`

Recommended: `0.40–0.50s`

Higher values are more permissive and may show weave windows when mh/oh swings are less tightly synced.

### Safe Window

The safe window shows when a hardcast should fit between the off-hand landing and the next main-hand swing.

- Green = chain lightning is available
- Blue = chain lightning is on cooldown, use lightning bolt instead

### Latency Padding

Spell thresholds adjust for your latency.

## Notes

- Built for WotLK 3.3.5a, using this version of WeakAuras: https://github.com/NoM0Re/WeakAuras-WotLK
- Private server behavior may vary.
- Melee context is detected from recent player white swings.
- If you are not actively meleeing, the weave UI should suppress fake ranged-cast swing cycles.

## changelog

### v0.1.0
