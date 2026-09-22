# NexusNote — Scroll-Driven Landing Animation

A 2D ink line-art scroll animation for the NexusNote landing page. A hand-drawn character writes on papers, carries each to a board, and pins them. The marks drawn on the four papers compose a triangle that fills yellow when complete — visualizing NexusNote's core idea: **connect your notes, make something new.**

## The Story (scroll sequence)

The animation plays as a single scroll-driven scene with four repeating cycles, then a finale:

1. **Write** — The character sits at a desk and writes a mark on a paper. The hand visibly draws the mark stroke-by-stroke with a pen and ink trail.
2. **Stand & walk** — The character stands, picks up the paper, and walks to the board.
3. **Pin** — The character pins the paper to the board at its slot.
4. **Walk back & sit** — The character returns to the desk for the next paper.

After the fourth paper is pinned, the triangle completes and fills yellow, then the finale plays: ink threads, tag chips, AI sparks, a light bulb lighting up, and the closing message.

## The Four Marks

Each paper carries one mark, drawn live by the character's hand during the writing cycle:

| Paper | Mark | Pinned at          |
|-------|------|--------------------|
| 1     | `^`  | Top vertex         |
| 2     | `<`  | Bottom-left vertex |
| 3     | `_`  | Base center        |
| 4     | `>`  | Bottom-right vertex|

The chevron angles are matched to the actual triangle geometry — each stroke runs parallel to the triangle edge it belongs to, so the four marks read as one continuous triangle.

## Triangle Formation

The triangle is not pre-drawn. It forms progressively as papers are pinned:

- **Paper 1 pins** → the left edge draws down from the top vertex (yellow).
- **Paper 2 pins** → the base draws across the bottom (yellow).
- **Paper 3 pins** → rests on the base (its `_` mark sits on the edge).
- **Paper 4 pins** → the right edge draws up, closing the triangle (yellow).

Once all three edges are drawn, the triangle **fills with yellow** (fades in behind the papers).

## Finale

After the triangle completes:

- Ink threads draw themselves between the pinned notes.
- Tag chips stamp onto the notes (Notes / Projects / Thoughts).
- Amber AI-attention sparks attach to the connected notes.
- A line-art light bulb flickers, then lights up.
- Closing message: *"Connect your notes. Make something new."*

## Technical Details

- **Style:** Clean 2D ink line art derived from Xbot motion capture. No particles, dots, or visible 3D-model aesthetic.
- **Character:** Shaped torso, tapered limbs, head, hands, shoes, gaze, pen — hand-drawn styling throughout.
- **Animation:** Walking and idle use motion-capture data where available; sitting, writing, pinning, and transitions are procedurally posed with CCD inverse kinematics (IK).
- **Hand tracking:** Hand-to-paper and hand-to-board corrections keep the pen on the paper during writing and the hand on the pin during pinning.
- **Scroll:** Smooth scroll-linked transitions across the whole sequence. Supports desktop, mobile, fast scrolling, and reduced-motion (static fallback).
- **First paint:** Correct on load — no invisible or un-triggered sections.
- **Marks:** Each mark is defined as UV-coordinate stroke segments traced by the hand; the trail is stored per-paper and re-rendered on the pinned note.

## Running It

No build step. Open `index.html` in a browser and scroll.

## Product Context

NexusNote is a private, encrypted personal knowledge workspace:

- Users create **Nexus nodes** — notes, projects, thoughts.
- **Tags** and **connections** form relationships between nodes.
- **AI items** attach to connected content.
- **AI Attention** = "my AI assistant should pay attention to this later."
- **Important** = "this matters to me personally or operationally."
- Planned MCP connections: ChatGPT, Claude, CLI agents.
- The dashboard is a command center, not random statistics.

Landing-page direction: minimal copy carried by a strong animation — this prototype.

## File

- `index.html` — the complete self-contained animation (markup, styles, and script in one file).
