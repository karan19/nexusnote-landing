# NexusNote — Scroll-Driven Landing Animation

A 2D hand-drawn scroll story for the NexusNote landing page: one person's relationship with their knowledge. Notes fly to a board as paper planes, the human chooses what matters, AI connects only what was chosen, and the story ends with who they're becoming.

## The Story

Three papers, each flipping physically into the next, then a finale.

### Paper 1 — "Connect the dots."
1. Three pairs fly to the board together: a note + a project, a thought + a project, a note + a thought. Notes, projects, and thoughts each have distinct small hand-drawn shapes.
2. The human taps three important nodes. Each chosen node gets a warm amber highlight ring and a small hand-drawn "AI tagged" chip.
3. The human taps the circular sparkles-only AI Attention button. An AI scan sweeps the selected items.
4. Connections draw only between the selected items, and those selected shapes resolve into a yellow triangle. An idea bulb appears.

The rule of this paper: the human chooses the important items and sends them to AI — the system never chooses for them.
Copy: "Connect the dots." / "save to NexusNote" / "Observe what it creates for you". A tiny "encrypted" lock badge sits in the frame's top-right corner.

### Paper 2 — "Make it stick."
The character chooses **"Design for peak, not average."** — reinforced across exactly two exposures (the second: "What should the system be designed to survive? Peak conditions."). Reinforcement is a distinct user-controlled action, separate from amber AI Attention: AI may discover something, but the user separately chooses what to reinforce.

### Paper 3 — "Become."
A person outline surrounded by contextual nodes (Ideas, Learning, Projects, Principles, Goals). Semantic connections form and the central figure becomes subtly more resolved. A philosophy beat, not another product-feature demo.

### Finale
- Lockup: **NexusNote** / "Connect what you know. Discover what you think." / "A better note-taking system for who you're becoming."
- The character sits pointing up with one finger toward the top-right — where login / sign up will live in the real product — with steady "Try now" text above the hand (no box, no jitter).

## Design rules
- One gender-neutral character: short dark hair, mustard sweater, loose dark navy trousers, white sneakers, relaxed open hands.
- Amber/gold means AI Attention; conviction uses ink, paper, and mustard.
- No tour of features, no chatbot bubbles, no second character, no robot/neural imagery.
- Privacy appears only as the tiny "encrypted" cue.

## Technical
- Canvas 2D, procedural, responsive, lightweight. The story reconstructs through `render(progress)` — scrolling up reverses everything; no irreversible click state.
- Papers flip physically into each other (no fades or teleports); board/character spatial relationships hold on mobile.

## Running it
No build step. Open `index.html` in a browser and scroll.

## Product context
NexusNote is a private, encrypted personal knowledge OS: Nexus nodes (notes, projects, thoughts), tags, connections, AI items. AI Attention ("my AI should pay attention to this") vs Important ("matters to me"). Planned MCP connections to ChatGPT, Claude, and CLI agents. Landing-page direction: minimal copy carried by a strong animation — this prototype.

## Changelog — 2026-09-23
- Replaced the four-paper / four-mark triangle with three paired flights (note+project, thought+project, note+thought) and the human-chooses-three flow: amber rings, "AI tagged" chips, a sparkles-only AI Attention button, and a triangle formed from the selected nodes.
- Added Paper 2 ("Make it stick." — "Design for peak, not average.", two reinforcement exposures, reinforcement as a user-controlled action) and Paper 3 ("Become." — contextual nodes around a resolving figure), joined by physical page flips.
- Rebuilt the finale: three-line lockup, a pointing figure cueing the top-right login/sign up placement, "Try now" text, and an "encrypted" lock badge on Paper 1. Removed the 3D board, its GIF, and the grid from the final slide.

## File
- `index.html` — the complete self-contained animation (markup, styles, and script in one file).
