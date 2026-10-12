---
name: Chase the Light
description: A quiet lake surface portfolio with a tactile web music player.
colors:
  lake-slate: "#708f9d"
  deep-lake: "#10292f"
  lake-teal: "#193d43"
  lake-ink: "#09282e"
  mist: "#f6f3eb"
  pale-leaf: "#deebd8"
  soft-mint: "#c2d9d5"
  muted-mint: "#a9c7bd"
  white-rule: "rgba(255,255,255,0.19)"
typography:
  display:
    fontFamily: "Georgia, Times New Roman, serif"
    fontSize: "clamp(64px, 8.7vw, 138px)"
    fontWeight: 400
    lineHeight: 0.96
    letterSpacing: "-5px"
  title:
    fontFamily: "Microsoft YaHei, Arial, sans-serif"
    fontSize: "28px"
    fontWeight: 400
    lineHeight: 1.35
  body:
    fontFamily: "Arial, Microsoft YaHei, sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.9
  label:
    fontFamily: "Arial, Microsoft YaHei, sans-serif"
    fontSize: "11px"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: "2px"
rounded:
  sm: "4px"
  md: "10px"
  lg: "16px"
  xl: "22px"
  pill: "30px"
spacing:
  xs: "8px"
  sm: "12px"
  md: "20px"
  lg: "28px"
  xl: "35px"
components:
  button-primary:
    backgroundColor: "{colors.pale-leaf}"
    textColor: "{colors.deep-lake}"
    rounded: "{rounded.md}"
    padding: "9px 13px"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.mist}"
    rounded: "{rounded.pill}"
    padding: "10px 14px"
  player-panel:
    backgroundColor: "{colors.lake-teal}"
    textColor: "{colors.mist}"
    rounded: "{rounded.xl}"
    padding: "28px"
  text-input:
    backgroundColor: "rgba(8,35,42,0.26)"
    textColor: "{colors.mist}"
    rounded: "{rounded.md}"
    padding: "12px 14px"
---

# Design System: Chase the Light

## Overview

**Creative North Star: "Listening at the Waterline"**

The interface treats the lake as both scene and material. A slate blue-green surface, translucent panels, soft mint controls, and serif display type create a calm portfolio that lets the work and the sound arrive gradually. The background is an active canvas: the lake, ripples, fish, and changing light remain visible behind the interface.

The portfolio is sparse and atmospheric. The player keeps that same world while becoming more functional: glassy decks and queues sit above the water, compact labels support scanning, and the record, timeline, lyrics, and queue provide tactile anchors.

**Key Characteristics:**

- Lake blue-green surfaces with pale plant-like highlights.
- Serif display headlines paired with restrained sans-serif UI text.
- Translucent glass layers and fine white rules instead of heavy borders.
- Motion is slow and purposeful: water, record rotation, hover drift, and day/night changes.
- Responsive layouts preserve the scene while collapsing player panels into a single column.

## Colors

The palette is a muted lake range: slate water for the ground, deep teal for readable surfaces, pale mint for actions, and warm off-white for type.

### Primary

- **Slate Lake** (#708f9d): Main page ground and the base tone behind the animated water.
- **Deep Lake** (#10292f): Dialog and deep surface background.

### Secondary

- **Lake Teal** (#193d43): Elevated player panels, project dialogs, and glass surfaces.
- **Pale Leaf** (#deebd8): Primary player actions, play controls, and selected states.

### Neutral

- **Mist** (#f6f3eb): Main display and interface text.
- **Soft Mint** (#c2d9d5): Supporting descriptions and metadata.
- **Muted Mint** (#a9c7bd): Secondary labels and low-emphasis copy.
- **White Rule** (rgba(255,255,255,0.19)): Dividers, outlines, and quiet structure.

**The Waterline Rule.** Keep the lake visible through transparent or translucent layers; opaque panels are reserved for readable dialogs and reduced-transparency preferences.

## Typography

**Display Font:** Georgia, Times New Roman, serif  
**Body Font:** Arial, Microsoft YaHei, sans-serif  
**Label Font:** Arial, Microsoft YaHei, sans-serif with tracked uppercase labels

**Character:** The serif display is reflective and editorial. The sans-serif UI remains plain, compact, and legible over moving water.

### Hierarchy

- **Display** (400, `clamp(64px, 8.7vw, 138px)`, `0.96`): Portfolio hero and major scene statements.
- **Headline** (400, `28px` in the player, around `36px` in dialogs): Player and project titles.
- **Body** (400, `15px`, `1.9`): Introductory copy and project descriptions.
- **Label** (400, `11–12px`, `2–3px` tracking, uppercase where marked): Eyebrows, metadata, times, and navigation support.

**The Two Voices Rule.** Use Georgia for expressive statements and the sans-serif stack for controls, metadata, and functional copy.

## Layout

The portfolio uses a full-viewport fixed lake canvas with content layered above it. Desktop content is positioned with generous viewport gutters (`5–10vw`) and a wide hero field. The works list is intentionally narrow (`260–340px`) and uses horizontal rules as its rhythm.

The web player uses a centered two-column workspace: a flexible deck and a narrow queue, capped around `980–1180px` and `90–94vw` wide. At `760px` and below it becomes one column; at `600px` and below the portfolio reduces type, gutters, and list width. Short viewports move the hero and footer into normal document flow so content remains reachable.

## Elevation & Depth

Depth comes from translucent teal layers, backdrop blur, radial and linear gradients, and restrained ambient shadows. Panels are lifted from the lake without becoming opaque cards. The record uses a circular shadow and repeating radial grooves as its tactile depth cue.

## Shapes

The portfolio uses mostly open edges and thin rules. Functional player elements use soft rounded rectangles (`10–16px`), dialogs and large decks use larger corners (`18–24px`), and sound controls, tags, and compact pills use fully rounded ends (`20–30px`). Focus rings are white, `2px`, and offset for visibility.

## Components

### Buttons

- **Primary:** Pale leaf fill with deep lake text, compact padding, and a soft rounded rectangle.
- **Ghost:** Transparent fill, light text, thin translucent rule, and pill shape where it acts as a compact control.
- **Hover / Focus:** Lighten the fill or raise the item slightly; keep the `2px` white focus outline and avoid aggressive bounce.

### Cards / Containers

- **Player panels:** Translucent deep teal gradient, backdrop blur, thin white rule, `24px` radius, and `28px` internal padding on desktop.
- **Stage:** Dark translucent inset with a `16px` radius; it holds the record, video, or empty state.
- **Queue:** Shares the deck surface language and becomes static below `760px`.

### Inputs / Fields

Search and dialog fields use a dark translucent lake background, `1px` white rule, `10–12px` radius, light text, and pale placeholder text. Focus remains visible through the shared white outline.

### Navigation

The portfolio navigation is minimal: a serif brand lockup, sound toggle, work links, and day/night time controls. The player navigation is the library tab row and the return link. On small screens, controls wrap or become a single-column flow while the lake canvas remains present.

### Lake Canvas and Record

The fixed `#lake` canvas is the signature background. The player record is a grooved circular surface with a pale center control and a slow spin while playing. Preserve reduced-motion behavior for users who request it.

## Do's and Don'ts

### Do:

- **Do** keep important text warm off-white or pale mint against deep teal surfaces.
- **Do** preserve the visible water, day/night switch, ripples, and fish interaction as part of the identity.
- **Do** use translucency, blur, and fine rules to separate layers.
- **Do** keep desktop and responsive pages visually synchronized.
- **Do** let mobile layouts collapse gracefully and remain usable at short heights.

### Don't:

- **Don't** introduce unrelated bright brand colors or generic purple-blue gradients.
- **Don't** cover the lake with opaque containers when a translucent layer is readable.
- **Don't** replace the serif display voice with a generic system heading.
- **Don't** use dense nested cards for portfolio content.
- **Don't** remove reduced-motion handling or visible keyboard focus states.
