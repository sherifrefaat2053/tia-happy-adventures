# AGENTS.md

## Project Identity

**Project name:** Tiya's Happy Adventures
**Project type:** Lightweight interactive HTML5 toddler game
**Primary audience:** A 3-year-old child named Tiya
**Core experience:** Tapping colorful balloons and butterflies to trigger cheerful animations, sounds, stars, and positive reactions from Tiya.

Read `README.md` completely before planning or changing any code.

---

## Product Goal

Build a joyful, polished, colorful, and extremely simple web game designed specifically for a 3-year-old child.

The game must:

* Be immediately understandable without written instructions.
* Work primarily through tapping.
* Never punish the player.
* Never show a game-over screen.
* Never create stressful countdowns or failure states.
* Celebrate every interaction.
* Feel visually polished and lively rather than like a basic coding demo.
* Be safe, calm, responsive, and suitable for repeated play.

The experience should prioritize delight, responsiveness, visual clarity, and emotional positivity over difficulty or competition.

---

## Core Game Loop

1. Colorful balloons and butterflies appear and move gently across the scene.
2. The player taps or clicks a balloon or butterfly.
3. The tapped object immediately reacts.
4. A cheerful pop or sparkle animation plays.
5. A child-friendly sound effect plays.
6. One glowing star is awarded.
7. Tiya performs a happy reaction such as cheering, smiling, waving, or jumping.
8. A new object appears and play continues indefinitely.

There must be no losing condition.

---

## Required Technology

Use only:

* HTML5
* CSS3
* Vanilla JavaScript

Do not introduce:

* React
* Vue
* Angular
* Phaser
* Canvas game engines
* Large animation libraries
* Heavy UI frameworks
* Build systems unless the repository already requires one
* Unnecessary npm dependencies

The game should run by opening `index.html` or through a very simple local development server.

Keep the project easy to understand, edit, and deploy as a static website.

---

## Recommended Project Structure

Prefer a clear structure similar to:

```text
/
├── index.html
├── README.md
├── AGENTS.md
├── css/
│   └── styles.css
├── js/
│   ├── game.js
│   ├── objects.js
│   ├── audio.js
│   └── character.js
├── assets/
│   ├── characters/
│   ├── balloons/
│   ├── butterflies/
│   ├── backgrounds/
│   ├── sounds/
│   └── ui/
└── tests/
```

Do not create unnecessary files or abstractions for a small project.

A simpler structure is acceptable when it keeps the code cleaner.

---

## Development Roadmap

Implement the project in controlled phases.

### Phase 1 — Foundation and Garden Scene

Create:

* Semantic HTML structure.
* Full-screen responsive game container.
* Bright garden environment.
* Layered background depth.
* Safe visible play area.
* Basic loading state if assets require loading.
* Responsive layout for mobile, tablets, and desktop.
* Large touch-friendly interactive zones.

Do not implement the full game logic during this phase unless explicitly requested.

### Phase 2 — Interactive Floating Objects

Implement:

* Balloon generation.
* Balloon movement.
* Butterfly generation.
* Butterfly movement.
* Tap and click interactions.
* Pop, sparkle, or disappearance animations.
* Automatic cleanup of removed objects.
* Object spawning that remains smooth and controlled.
* Protection against duplicate scoring from repeated taps.

### Phase 3 — Tiya Character Integration

Implement:

* Tiya character rendering.
* Idle animation.
* Happy reaction animations.
* Reaction after successful taps.
* Character positioning that never blocks gameplay.
* Smooth switching between idle and reaction states.
* Sound effects that comply with browser autoplay restrictions.

Do not create, redesign, or modify Tiya’s appearance without an approved character sheet.

### Phase 4 — Stars and Final Polish

Implement:

* Glowing star score display.
* Positive score animation.
* Improved touch responsiveness.
* Better object variety.
* Subtle visual effects.
* Audio controls.
* Performance optimization.
* Cross-device testing.
* Final mobile and tablet polish.

Do not implement phases outside the current requested scope.

---

## Tiya Character Rules

Tiya is the hero and must remain visually consistent.

When a character sheet or reference images are provided:

* Treat them as the single source of truth.
* Preserve Tiya’s facial features.
* Preserve hairstyle.
* Preserve skin tone.
* Preserve body proportions.
* Preserve clothing unless a change is explicitly requested.
* Preserve the established visual style.
* Do not replace Tiya with a generic child character.
* Do not use random AI-generated versions of Tiya.
* Do not change her identity between animation states.

Allowed changes include:

* Facial expressions.
* Hand gestures.
* Small body movements.
* Jumping.
* Cheering.
* Waving.
* Looking toward tapped objects.

Do not distort, stretch, crop, or recolor the character assets.

If the character sheet has not been added yet:

* Use a clearly labeled temporary placeholder.
* Keep character integration modular.
* Do not invent a permanent character design.
* Make replacement with the final assets straightforward.

---

## Visual Direction

The game should look like a polished children’s game, not a basic website.

### Theme

Use a cheerful magical garden with:

* Flowers.
* Soft grass.
* Clouds.
* Trees or bushes.
* Sparkles.
* Gentle floating particles.
* Friendly balloons.
* Cute butterflies.
* Soft depth and layering.

### Color Direction

The visual palette should primarily use:

* Pink.
* Purple.
* Soft blue.
* Light green.
* Warm yellow.
* White highlights.

Colors should be vibrant but not harsh or visually exhausting.

### Visual Quality Rules

* Avoid generic gradients used without purpose.
* Avoid cluttered layouts.
* Avoid excessive glow.
* Avoid dark or scary elements.
* Avoid sharp aggressive shapes.
* Avoid overly realistic imagery.
* Avoid generic AI-looking decorative elements.
* Avoid tiny details that are unclear on mobile.
* Avoid interfaces that resemble admin dashboards or ordinary websites.
* Maintain clear visual hierarchy.
* Use smooth rounded shapes.
* Use soft shadows carefully.
* Keep the main interactive objects visually dominant.

---

## User Interface Rules

The UI must be suitable for a 3-year-old.

Use:

* Large interactive elements.
* Large tap targets.
* Clear visual reactions.
* Minimal text.
* Icon-based controls.
* Rounded friendly shapes.
* Strong visual separation between interactive and decorative elements.

Avoid:

* Small buttons.
* Text-heavy instructions.
* Menus with multiple levels.
* Keyboard-dependent controls.
* Complex settings.
* Tiny close icons.
* Hover-only interactions.
* Precision-based tapping.
* Competitive leaderboards.
* Negative messages.

The star score should be represented visually using glowing stars.

A number may appear alongside the stars only if it remains easy to understand.

---

## Interaction Rules

Support:

* Touch input.
* Pointer input.
* Mouse clicks.

Use Pointer Events where practical to avoid maintaining separate touch and mouse logic.

Every successful tap must provide immediate feedback.

Target response time should feel instant.

Interactive objects must:

* Have generous hit areas.
* Be easy to tap even while moving.
* Ignore accidental repeated input after being activated.
* Never become impossible to reach.
* Avoid spawning underneath essential UI controls.
* Avoid moving too quickly.
* Avoid overlapping excessively.

Do not require:

* Dragging.
* Swiping.
* Multi-touch gestures.
* Double tapping.
* Keyboard input.
* Precise timing.

---

## Game Difficulty and Emotional Safety

This project must not behave like a competitive or difficult game.

Do not add:

* Lives.
* Health bars.
* Failure sounds.
* Red error messages.
* Game-over states.
* Time pressure.
* Miss penalties.
* Score reductions.
* Scary characters.
* Loud sudden sounds.
* Frustrating object speeds.
* Ads.
* External links visible during play.
* In-app purchases.
* Data collection.

Missing an object should have no negative consequence.

The player should always feel successful.

---

## Animation Rules

Animations should be:

* Smooth.
* Cheerful.
* Short.
* Easy to understand.
* Lightweight.
* GPU-friendly where possible.

Prefer animating:

* `transform`
* `opacity`

Avoid frequent animation of expensive layout properties.

Support `prefers-reduced-motion` by reducing decorative motion without disabling core interaction feedback.

Typical reactions may include:

* Scale pop.
* Small rotation.
* Sparkle burst.
* Star trail.
* Gentle bounce.
* Tiya cheer.
* Floating star toward the score display.

Avoid excessive screen shaking, flashing, or rapid movement.

---

## Audio Rules

Audio must be cheerful, soft, and suitable for a toddler.

Use sounds for:

* Balloon pops.
* Butterfly sparkles.
* Star rewards.
* Tiya reactions.
* Optional soft background ambience.

Rules:

* Do not autoplay sound before the first user interaction.
* Initialize or resume audio only after a tap or click.
* Provide a clear sound on/off control.
* Start at a safe, moderate volume.
* Avoid loud, sharp, or startling sounds.
* Avoid playing too many sounds simultaneously.
* Prevent overlapping audio from becoming noisy.
* Reuse lightweight audio assets when appropriate.
* Keep the game playable with sound disabled.

Do not use copyrighted music or audio without confirmed permission.

---

## Responsive Design Requirements

The game must work correctly on:

* Mobile phones.
* iPads.
* Android tablets.
* Desktop browsers.
* Portrait orientation.
* Landscape orientation.

Primary design priority:

1. Tablet portrait.
2. Mobile portrait.
3. Tablet landscape.
4. Desktop.

Requirements:

* Use the full available viewport.
* Avoid horizontal scrolling.
* Respect mobile safe areas.
* Prevent important UI from sitting under notches or browser controls.
* Use responsive sizing with `clamp()`, percentages, viewport units, or container-based calculations.
* Keep Tiya fully visible.
* Keep the star score visible.
* Keep game objects inside usable screen boundaries.
* Recalculate positions after resize or orientation change.
* Prevent accidental page scrolling during gameplay.
* Avoid relying only on `100vh` where mobile browser UI may cause layout problems.
* Prefer modern viewport units such as `dvh` with a safe fallback.

---

## Performance Requirements

The game must remain lightweight and smooth.

Target:

* Fast initial load.
* Smooth animation on ordinary mobile devices.
* No memory leaks during extended play.
* No continuous creation of unused DOM elements.
* No unnecessary network requests.
* No excessive event listeners.
* No oversized image or audio files.
* No heavy frameworks.

Implementation rules:

* Remove popped objects from the DOM.
* Reuse objects where useful, but do not overengineer.
* Pause or reduce activity when the browser tab is hidden.
* Use `requestAnimationFrame` for custom animation loops.
* Avoid uncontrolled `setInterval` loops.
* Limit the maximum number of active objects.
* Compress visual and audio assets appropriately.
* Use WebP, AVIF, SVG, or optimized PNG where suitable.
* Preload only essential assets.
* Lazy-load nonessential assets when possible.

---

## Accessibility and Usability

Although the game is designed for a toddler, basic accessibility must still be respected.

* Give controls accessible labels.
* Ensure sound controls are understandable.
* Maintain sufficient visual contrast.
* Do not communicate important state using color alone.
* Keep focus styles for keyboard accessibility.
* Use semantic buttons for controls.
* Avoid flashing content.
* Respect reduced-motion preferences.
* Do not trap focus.
* Ensure decorative images do not produce unnecessary screen-reader noise.

Core gameplay may remain touch-first.

---

## Browser Support

Support current versions of:

* Google Chrome.
* Microsoft Edge.
* Safari.
* Mobile Safari.
* Chrome for Android.

Do not rely on experimental browser features without graceful fallbacks.

The game must not produce console errors during normal use.

---

## Coding Standards

* Use clear and descriptive names.
* Keep functions focused.
* Avoid deeply nested logic.
* Avoid global variables where practical.
* Separate game state from DOM rendering where useful.
* Use constants for configurable values.
* Add comments only where behavior is not self-explanatory.
* Do not duplicate logic.
* Keep configuration values centralized.

Useful configurable values may include:

* Spawn interval.
* Maximum active objects.
* Balloon speed range.
* Butterfly speed range.
* Sound volume.
* Reaction duration.
* Star animation duration.
* Object size range.

Do not overengineer the architecture.

This is a small game and should remain easy to maintain.

---

## Asset Management

All assets must be stored inside the repository unless explicitly approved otherwise.

Do not depend on unstable external image URLs.

Use organized asset folders.

File names should be:

* Lowercase.
* Descriptive.
* Hyphen-separated.
* Free from unnecessary spaces.

Example:

```text
assets/characters/tiya-idle.webp
assets/characters/tiya-cheer.webp
assets/sounds/balloon-pop-01.mp3
assets/sounds/star-reward.mp3
```

Do not commit:

* Original uncompressed working files unless required.
* Huge PSD or design source files without a clear reason.
* Secrets.
* API keys.
* Temporary exports.
* Duplicate unused assets.
* `node_modules`.
* Local editor files.
* Operating system cache files.

---

## Security and Privacy

The game should be fully client-side unless a backend is explicitly requested.

Do not add:

* Tracking scripts.
* Analytics.
* Cookies.
* Login systems.
* User accounts.
* Advertising SDKs.
* Third-party data collection.
* Camera access.
* Microphone access.
* Location access.
* External chat services.

Do not collect or transmit information about the child.

Never commit credentials or secret values.

---

## Git Workflow

Before changing code:

1. Read `AGENTS.md`.
2. Read `README.md`.
3. Inspect the full repository.
4. Check the current project status.
5. Identify the exact requested phase.
6. Present a concise implementation plan when the task is substantial.

During work:

* Keep changes focused.
* Do not modify unrelated files.
* Do not delete working functionality without a clear reason.
* Do not push directly to `main`.
* Use a dedicated branch when branch creation is available.
* Use clear commit messages.
* Avoid mixing unrelated changes in one commit.

Suggested branch names:

```text
phase-1-garden-foundation
phase-2-floating-objects
phase-3-tiya-character
phase-4-star-system
fix-mobile-touch
fix-audio-playback
```

Suggested commit style:

```text
feat: create responsive garden game scene
feat: add tappable floating balloons
feat: integrate Tiya reaction states
feat: add glowing star score system
fix: improve touch targets on tablets
perf: remove inactive game objects
```

---

## Required Verification

After every implementation task, run all relevant available checks.

At minimum verify:

* The game opens successfully.
* No console errors appear.
* Objects spawn correctly.
* Objects can be tapped.
* A single object cannot award multiple stars.
* Popped objects are removed correctly.
* The score updates correctly.
* Tiya reacts correctly.
* Sound starts only after user interaction.
* Sound mute works.
* The layout has no horizontal scroll.
* Portrait mode works.
* Landscape mode works.
* Mobile touch works.
* Tablet touch works.
* Desktop click works.
* Resizing does not break object positions.
* Extended play does not continuously increase DOM elements.
* Essential controls remain visible.
* No object blocks the entire playable area.

When browser automation is available, test representative viewport sizes such as:

```text
390 × 844   Mobile portrait
844 × 390   Mobile landscape
768 × 1024  Tablet portrait
1024 × 768  Tablet landscape
1440 × 900  Desktop
```

Do not claim that a test passed unless it was actually run.

If a test could not be run, state that clearly.

---

## Manual Testing Checklist

For each completed phase, manually confirm:

### Gameplay

* Objects are easy to notice.
* Objects are easy to tap.
* Feedback appears immediately.
* No tap creates a negative response.
* New objects continue appearing.
* The game remains fun without explanation.

### Visual Quality

* The garden feels polished.
* Tiya is visually prominent but does not block gameplay.
* Colors are bright but comfortable.
* The interface does not feel like a template.
* Decorative elements do not distract from interactive objects.
* Text is minimal and readable.

### Mobile and Tablet

* No accidental page scrolling occurs.
* No element is cropped unexpectedly.
* Score remains visible.
* Audio control remains accessible.
* Touch targets are large enough.
* Orientation changes do not break the layout.

### Performance

* Motion remains smooth.
* No major frame drops occur.
* Audio does not become chaotic.
* The number of active elements remains controlled.
* Long play sessions do not cause obvious slowdown.

---

## Change Restrictions

Do not:

* Rewrite the entire project for a small feature.
* Introduce a framework without explicit approval.
* Replace approved visual assets.
* Change Tiya’s identity.
* Add text-heavy tutorial screens.
* Add competitive mechanics.
* Add failure states.
* Add login or online features.
* Add analytics or tracking.
* Add external dependencies without explaining why they are necessary.
* Add placeholder features and describe them as complete.
* Ignore mobile and tablet testing.
* declare the work complete with failing tests or console errors.

---

## Handling Missing Information

When a required asset or decision is missing:

* Continue with the parts that can be implemented safely.
* Use a clearly marked temporary placeholder where necessary.
* Keep the implementation ready for later asset replacement.
* List the missing item in the final report.
* Do not invent permanent brand or character decisions.
* Do not block the entire task over a noncritical missing detail.

For Tiya’s final appearance, always wait for the approved character sheet.

---

## Final Response Format

After completing a coding task, provide:

1. **Implemented scope**
2. **Files created**
3. **Files modified**
4. **Files deleted**
5. **Gameplay behavior added**
6. **Responsive behavior**
7. **Commands executed**
8. **Tests and checks performed**
9. **Test results**
10. **Manual verification steps**
11. **Known limitations**
12. **Recommended next phase**

Be precise.

Do not claim the project is fully complete when only one phase was implemented.

---

## Definition of Done

A phase is complete only when:

* The requested phase is fully implemented.
* The game opens without errors.
* The requested interactions work.
* Touch and click input work correctly.
* The layout works across target viewport sizes.
* No horizontal overflow exists.
* No obvious memory leak is present.
* Active objects are cleaned up correctly.
* Audio behavior follows browser restrictions.
* Existing functionality remains working.
* Relevant documentation is updated.
* Tests and verification results are reported honestly.
* The changes are ready for human review.

The final result should feel like a real, joyful children’s game made especially for Tiya, not a generic web development exercise.
