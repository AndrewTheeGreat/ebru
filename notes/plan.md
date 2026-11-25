# Build plan — Ebru

Deliverable: `ebru.html`, one self-contained file. Open it in a browser. No build step.

## Milestones
1. **Engine (working early).** Ink regions are closed polygons. Operations transform every vertex:
   - drop: `P' = C + (P−C)·√(1 + r²/|P−C|²)` (exact, area-preserving, composes by adding r²)
   - line comb: `P' = P + z·e^(−|d|/c)·M` with tines repeating every `s` (optionally wavy)
   - stylus / finite comb: a local smudge with exponential falloff
   - vortex: rotation whose angle decays with radius
   Adaptive resampling keeps edges ~2px on screen and coarse off screen. Covered layers get pruned.
2. **Interaction.** Five tools (drop, sprinkle, stylus, comb, swirl), palettes, undo, skim.
3. **Recipes as generators.** Battal, Gelgit, Taraklı, Tavus, Hatip, Lale, Suminagashi, Girdap, with animated comb/needle ghosts and captions. The demo plays Tavus on load.
4. **Sound.** WebAudio only: rising "bloop" + pentatonic ring per drop, noise scrape that follows stylus speed, a paper rustle, reverb.
5. **Print ritual.** A sheet lowers onto the bath, ink soaks through, the sheet peels away, and the print comes out mirrored with grain, pinholes and a deckled edge. It hangs on a clothesline that persists in localStorage. Download as PNG.
6. **Test + polish.** Check it in the browser, look at perf, mobile layout and edge cases, then tune the first 10 seconds.
