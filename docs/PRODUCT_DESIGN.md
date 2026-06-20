# Life Replay AI — The Complete Product Design System

> **Document type:** Master Experience & Interface Design Specification
> **Owner:** Head of Product Design (composite mandate — Apple · Instagram · Spotify · Airbnb · OpenAI)
> **Status:** v1.0 — Design source of truth
> **Scope:** End-to-end UX, IA, screen design, interaction design, visual language, motion, growth, monetization, and self-critique.
> **Constraint:** This is a design document. No code. Every section is implementation-ready for engineering, but expressed in product and design language.

---

## How To Read This Document

This document is organized as twelve parts, exactly mirroring the brief, plus a foundational preamble. It is written to be read by four audiences simultaneously:

1. **Designers** — who need pixel-level, motion-level, and interaction-level specificity.
2. **Engineers** — who need to understand data dependencies, states, edge cases, and performance budgets.
3. **Product leaders** — who need to understand *why* each decision exists and how it maps to retention, emotion, and revenue.
4. **Founders / executives** — who need the narrative and the bet.

Wherever a screen is described, it is described in five layers:

- **Purpose** — why this screen exists at all. If it can't justify itself, it gets cut.
- **Emotional target** — the single feeling the user should walk away with.
- **Layout & hierarchy** — what is on screen, in what order, at what weight.
- **Interaction & motion** — what happens when the user touches, scrolls, holds, swipes, waits.
- **Edge cases & states** — empty, sparse, loading, error, offline, first-run, power-user.

---

## Preamble: What Life Replay AI Actually Is

Most apps help you *do* something. Life Replay AI helps you *feel* something — specifically, it helps you feel the weight, beauty, and arc of your own life.

The product ingests the exhaust of a modern life — photos, location history, health and fitness data, sleep, music, calendar, notes, messages metadata, financial milestones, screen time — and transforms that raw, chaotic data into **a narrated, cinematic, emotionally intelligent story of who you are and who you are becoming.**

It is three products fused into one:

- A **memory engine** (Apple Photos' Memories, but with a soul and a narrator).
- A **life analytics engine** (Spotify Wrapped, but every day, about everything).
- A **personal AI biographer** (a companion who has read your entire life and can talk to you about it).

The competitive insight is this: every tech company is sitting on a goldmine of personal data and uses it to optimize *engagement metrics for advertisers*. Life Replay AI uses that exact same data to do the one thing those companies never do — **give the meaning back to the person it belongs to.**

### The One-Sentence Product

> **Life Replay AI turns your life into a movie you can watch, a story you can share, and a companion you can talk to — and it makes you fall in love with your own existence.**

### The Three Emotional Pillars

Every single design decision in this document is downstream of three emotional pillars. If a feature does not serve one of these, it does not ship.

1. **REVERENCE** — "My life is bigger and more beautiful than I realized."
   The product treats the user's life as sacred material. The tone is never gamified-cheap, never gimmicky. It is cinematic, warm, and quietly awed by the person using it.

2. **REVELATION** — "I just learned something true about myself."
   The product's superpower is pattern recognition across time. Humans cannot see their own multi-year arcs. The app can. Every session should risk surfacing one genuine, non-obvious truth.

3. **RETURN** — "I want to come back tomorrow to see what it shows me."
   The product manufactures a daily reason to return that is *emotional*, not *obligatory*. Streaks are the floor, not the ceiling. The real hook is: *what will my life show me today?*

### The Anti-Goals (What We Refuse To Be)

A great product is defined as much by what it refuses as what it builds.

- **We are not a social network.** There is no feed of other people. No likes from strangers. No follower count. The only person you compare yourself to is your past self. Comparison-with-others is the original sin of modern apps; we are built on comparison-with-self, which produces growth instead of anxiety.
- **We are not a productivity tool.** We do not make you feel behind. We have no "inbox zero" energy. We never shame.
- **We are not a data dashboard.** Numbers serve story. We never lead with a chart when we can lead with a moment.
- **We are not infinite-scroll dopamine.** Sessions are designed to have a *beginning, middle, and a satisfying end.* We want the user to put the phone down feeling fuller, not emptier.
- **We are not a surveillance product that feels like one.** Privacy is not a settings page; it is a felt emotional guarantee present in the visual language itself.

---

## Design North Stars (The Five Laws)

These are the constitutional laws of the product. Every reviewer, in every design critique, has the authority to reject work that violates them.

**Law 1 — Lead with emotion, support with data.**
The hero of every screen is a moment, a face, a memory, a feeling. Numbers are the supporting cast. We never open with a bar chart when we could open with "One year ago today, you were here."

**Law 2 — The product is a narrator, not a database.**
Everything is phrased as if a warm, intelligent, slightly poetic friend is showing you your life. "You walked 2,847 steps" is database language. "You barely left the house this week — and that's okay, last March looked the same right before things changed" is narrator language.

**Law 3 — Earn the wow before you ask for anything.**
We never ask for a subscription, a share, or a permission before we have delivered a genuine emotional payoff. Value precedes extraction, always.

**Law 4 — Cinematic by default.**
Motion, depth, light, and sound are not decoration. They are how the product signals reverence. Static = cheap. Cinematic = sacred.

**Law 5 — Every session ends on a high.**
We architect closure. No dead ends, no empty voids. The last thing a user sees in any flow is a moment of beauty, a small reward, or a gentle hook toward tomorrow.

---

# PART 1 — CORE PRODUCT EXPERIENCE

This part answers four questions: What is the first emotional moment? How do we manufacture a "wow" inside 60 seconds? How do we evoke the five target emotions — nostalgia, happiness, achievement, curiosity, personal growth? And what does *every* core interaction feel like?

## 1.1 The First Emotional Moment — Before The User Even Signs Up

The first emotional moment does not happen inside the app. It happens in the **App Store listing and the first launch animation**, and we design both as part of the experience.

**The App Store promise.** The hero copy is not "Track your memories." It is:

> **"Watch the movie of your life."**

The preview video is 12 seconds: a person's real photos, locations, and workouts assembling themselves — like iron filings snapping to a magnet — into a cinematic timeline that then *plays itself back* as a film, with a soft piano score and a single line of narration: *"This is the year you became yourself."* The user's emotional state before download is already set to *anticipation of meaning*.

**The cold-open launch.** On first launch, before any login form, the screen is near-black (`#08080C`). A single point of warm light blooms in the center. Then, one line of text fades up, letter by letter, kerned wide:

> *"You've lived 11,318 days."*

(The number is computed from a single question we ask first — birth year — or a sensible default that resolves the instant we get real data.)

A beat. Then:

> *"Let's go find the ones that mattered."*

The light expands into the onboarding. **We have made a promise in under five seconds: this app thinks your life is significant.** No competitor opens this way. Instagram opens with a login form. We open with reverence.

## 1.2 The 60-Second Wow — "The Genesis Replay"

The single most important sequence in the entire product is what happens in the first 60 seconds *after we get data access.* We call it the **Genesis Replay**. It is the moment that decides retention. Everything else in this document is in service of making this moment land.

Here is the minute, second by second.

**Seconds 0–8 — The Permission, Reframed.**
We do not show a wall of toggles. We show one screen: a slow, beautiful animation of photos, map pins, heart-rate lines, and music notes drifting like dust motes in a dark room. Centered text:

> *"To build your movie, I need to look through your memories. I'll never share them. They're yours."*

A single primary button: **"Show me my life."** Tapping it triggers the OS permission sheets (Photos, Health, Location) in a sequence we've ordered by emotional payoff — Photos first (highest emotional density, highest grant rate). We explicitly frame privacy *in the same breath* as the ask, because trust is the precondition for everything.

**Seconds 8–22 — The Gather (the "magic is happening" moment).**
This is the most technically important deception of delight in the product. Indexing a photo library takes real time. Instead of a spinner, we show **the gathering**: the user's *actual* thumbnails begin flying in from the edges of the screen, swirling into a slowly rotating sphere of their own life. As each cluster lands, a tiny label whispers up and fades: *"2,431 photos found." … "Found a trip to Lisbon." … "You took 412 photos in one week last summer — something happened."*

This does three things at once: (1) it makes latency feel like *magic instead of waiting*, (2) it proves instantly that we actually read their data, and (3) it plants the first hook of curiosity — *what happened that week?* The sphere is rendered with depth-of-field blur and warm bloom lighting. It looks expensive. It looks like the data is *alive*.

**Seconds 22–50 — The Genesis Replay itself.**
The sphere collapses into a single point and *detonates softly* into a 25-second auto-playing cinematic film — the user's first Replay, generated on the spot. It is structured as a three-act micro-film:

- **Act I — "Where you started."** The oldest photos we can find, slightly desaturated, warm grain, slow Ken Burns push-ins. Narration (text on screen, optionally voiced): *"This is one of the earliest moments in your library. Look how far you've come."*
- **Act II — "The middle."** A rapid, rhythm-cut montage synced to a swelling instrumental — peaks of activity, faces that recur (we detect the most-photographed person and feature them), a location you returned to again and again. *"Some people kept showing up. Some places became home."*
- **Act III — "Now."** The most recent photos, full saturation, crisp. The music resolves. Final card: *"This is just the trailer. Your full life is inside."*

This is the wow. The user has been in the app for under a minute and has *already watched a trailer for their own life that made them feel something.* They did not configure anything. They did not learn an interface. The product gave before it asked.

**Seconds 50–60 — The Soft Landing & The Hook.**
The film ends on the Home screen, which gently materializes *behind* the final card. The first thing the user sees on Home is a single card: **"This Day Last Year"** — already populated, already emotional. And a subtle, non-blocking prompt: *"Come back tomorrow — I'll have something new for you."* We have closed the loop: wow delivered, return seeded.

### Why this works (the psychology)

- **Peak-end rule:** the session has an intense emotional peak (the film) and ends on a warm, forward-looking note. Users remember experiences by their peak and their end; we engineered both.
- **Endowment effect:** by showing the user *their own* content immediately, we transfer ownership. It's not "an app," it's "my movie."
- **Curiosity gap:** "something happened that week" is an open loop the brain wants to close. The user now has a reason to explore.
- **Reciprocity:** we gave a genuine gift (a beautiful film) before asking for payment, sharing, or even a tour.

## 1.3 Engineering The Five Emotions

The brief names five emotions. Below, each is treated as a *designable system* — with the trigger, the mechanic, the UI surface, and the failure mode to avoid.

### 1.3.1 Nostalgia

**Definition we design for:** the bittersweet warmth of re-contacting a past self.

**Triggers we build:**
- **Temporal anchoring** — "This Day Last Year," "5 Years Ago Today," "The summer of 2022." Specific dates are more powerful than vague ranges; the brain time-travels harder with a precise coordinate.
- **Sensory re-immersion** — when surfacing an old memory, we recreate its *context*: the music that was popular then (or that the user listened to then, if we have it), the weather, the season's color grade. Nostalgia is multi-sensory; flat photos under-deliver.
- **The "you forgot this" mechanic** — we deliberately surface low-frequency memories the user has *not* looked at recently. The emotional payload of a forgotten memory is 5–10x a remembered one.

**UI surface:** warm color grade (slightly lifted blacks, golden highlights), film grain texture, a typographic style we reserve *only* for memories (a humanist serif, see Part 9). Nostalgia content is visually distinct from "today" content so the brain knows it's traveling back.

**Failure mode to avoid:** nostalgia tipping into grief. We detect potentially painful content (see Part 1.5, Emotional Safety) and never ambush the user with a deceased pet, an ex, or a hospital. Reverence requires care.

### 1.3.2 Happiness

**Definition we design for:** in-the-moment delight and the re-experiencing of joy.

**Triggers we build:**
- **The smile-detection highlight reel** — we surface the photos where the user (and people they love) are genuinely laughing. Joy is contagious across time.
- **Surprise-and-delight micro-moments** — unexpected confetti is cheap; unexpected *recognition* is priceless. "You've now visited 12 countries." "This is your 500th workout." The product notices things the user is proud of.
- **Momentum visualization** — happiness is partly the feeling of things going right. Showing an upward trend ("your mood has climbed for 3 weeks") produces present-tense happiness.

**UI surface:** brighter, higher-key compositions; faster, bouncier motion curves; the only place we permit playful particle effects.

**Failure mode to avoid:** forced positivity. If someone's data shows a hard month, pretending otherwise destroys trust. We are warm, not delusional.

### 1.3.3 Achievement

**Definition we design for:** the earned pride of having done something hard, over time.

**Triggers we build:**
- **Milestone detection** — distances run, books finished, weights lifted, places traveled, streaks held, money saved. We aggregate the invisible accumulation of effort into a single legible number.
- **The "you did this" framing** — credit is always assigned to the *user*, never the app. "You ran the distance of a marathon this month" not "Your stats updated."
- **Permanent trophy objects** — achievements aren't ephemeral toasts; they become collectible cards in a personal **Achievements vault** (see Part 7) with real visual weight — embossed, metallic, dated. Scarcity and permanence make them matter.

**UI surface:** materials that signal value — brushed metal, depth, weight, a satisfying physical "thunk" of motion and haptics when a milestone card seats into place.

**Failure mode to avoid:** trophy inflation. If everything is an achievement, nothing is. We rate-limit milestones and reserve the heavy visual treatment for genuinely rare ones.

### 1.3.4 Curiosity

**Definition we design for:** the itch to find out something about your own life you don't yet know.

**Triggers we build:**
- **Open loops** — "Something happened the week of July 14th. Tap to remember." We surface anomalies in the data (a spike in photos, a new location, a change in routine) as *questions*, not answers.
- **Personalized "did you know"** — the AI Companion (Part 8) surfaces non-obvious correlations: "You sleep better in weeks you walk more than 40k steps." The user didn't know that about themselves. Now they want to know more.
- **The locked-door mechanic** — some insights are gated behind "we need a bit more of your year to know this." Anticipation is a curiosity engine.

**UI surface:** a distinct "discovery" treatment — a soft pulsing glow, a question-mark-adjacent affordance, content that is partially obscured/blurred until tapped (the reveal is the reward).

**Failure mode to avoid:** clickbait that doesn't pay off. Every open loop *must* close with something genuinely interesting, or curiosity converts to distrust.

### 1.3.5 Personal Growth

**Definition we design for:** the felt sense that you are becoming a better, fuller version of yourself.

**Triggers we build:**
- **Then-vs-now comparisons** — always self-vs-self. "A year ago you ran a 12-minute mile. Now it's 9:40." Growth is only legible against a baseline; we always provide the baseline.
- **Narrative arc detection** — the AI identifies *chapters* in the user's life ("The Rebuilding Year," "The Year You Got Strong") and names them. Naming an arc makes growth feel real and authored.
- **Forward-looking reflection** — gentle prompts that invite intentionality: "You've grown a lot this year. What do you want next year to be about?" Growth is future-oriented, not just retrospective.

**UI surface:** side-by-side and overlay comparisons; the "arc" visual motif (a rising line that becomes a path); reflective, calm typography and pacing — growth content is *slow* content, never rushed.

**Failure mode to avoid:** turning growth into pressure. We celebrate progress without implying the user is insufficient. The tone is "look how far you've come," never "look how far you have to go."

## 1.4 The Core Interaction Vocabulary

Every great product has a small set of signature interactions that become muscle memory and identity. Ours:

- **The Hold-to-Replay.** Press and hold *any* memory, day, or card anywhere in the app, and it begins to play as a mini-Replay under your finger — a living, breathing preview. Release to stop, swipe up to expand to full screen. This is our equivalent of the iPhone's "press home to unlock" — a single gesture that defines the product. It teaches the core truth of the app: *everything here is alive and can be played.*
- **The Pull-to-Remember.** On Home and Timeline, pulling down doesn't just refresh — it *travels back in time*. The further you pull, the further back you go, with the date readout scrubbing and the background color-grading shifting warmer/older. Release to land on a memory from that era. Refresh becomes time travel.
- **The Pinch-to-Zoom-Through-Time.** On the Timeline, pinching doesn't zoom an image — it changes *temporal resolution* (life → decade → year → month → week → day). One continuous gesture moves you through every scale of your existence. (Detailed in Part 4.)
- **The Tap-to-Narrate.** Tap the small narrator orb present on memory screens and the AI speaks/writes a one-line reflection about what you're looking at. The product can always tell you *why this matters.*
- **The Swipe-to-Dismiss-Gently.** Nothing is deleted with violence. Swiping a card away animates it folding into a soft archive, with an undo always available. We never make the user feel they destroyed a memory.

These five gestures are introduced progressively (not in a tutorial dump) and become the user's intuitive language for the entire app.

## 1.5 Emotional Safety (The Invisible System That Makes Trust Possible)

A product that surfaces your past *will* eventually surface pain. How we handle this is the difference between "magical" and "cruel." This system runs under everything.

- **Sensitive-content detection.** We classify potentially painful memories — detected via clusters around hospitals, funeral homes, sudden gaps after a recurring face disappears, user-tagged people, calendar events, breakup-pattern signals. These are never auto-played in a Replay or pushed as a notification without consent.
- **The gentle gate.** When we believe a memory may be heavy, we don't hide it (that's patronizing) — we *announce and ask*: "There are memories here from a hard time. Would you like to see them?" The user is always in control of the door.
- **Person muting.** One tap to say "I'm not ready to see [person] right now." The app respects it everywhere, instantly, with no judgment and a clear path to unmute later.
- **No notifications on hard anniversaries** unless the user opts in. A death anniversary surfacing as a cheerful "On this day!" push would be unforgivable. Our calendar of the user's life includes a calendar of their grief.

This system is invisible when things are light and indispensable when things are heavy. It is the reason users will trust us with their whole lives.

## 1.6 The Daily Loop (The Macro-Interaction)

Zooming out from individual screens: what does a *typical day* with the product feel like?

1. **The morning whisper (optional push).** Not "You haven't opened the app." Instead: *"Good morning. One year ago today was a good one — want to see?"* The notification itself is a gift, not a guilt trip. It contains a thumbnail of the actual memory, so even ignoring it delivers a micro-hit of warmth.
2. **The open.** Lands on Home. Top card is "Today's Memory" — the single best thing the app wants to show today. 10-second emotional payoff available instantly.
3. **The optional deepening.** If the user has 2 minutes, they pull into a Replay, explore the Timeline, or ask the Companion something. If they have 10 seconds, the top card alone was worth it.
4. **The close on a high.** Every session, however short, ends with the app having shown the user something good about their own life. The dopamine is *meaning*, not novelty-slop.
5. **The evening reflection (optional).** A gentle end-of-day prompt: "How was today?" — one tap on a mood, optionally a sentence. This is the *only* active input we ask for, and it's framed as journaling-for-yourself, which compounds the data and the emotion.

The genius of the loop is that **it works at every time budget** — 10 seconds or 10 minutes — and *always* ends on a high. That is how a product becomes a daily habit without being a slot machine.

---

# PART 2 — INFORMATION ARCHITECTURE

The brief proposes: Home, Timeline, Stories, Replay, Insights, Profile. Six tabs is too many. The most important IA decision in this product is **restraint** — every tab dilutes the others. After modeling the navigation against the daily loop, here is the final architecture and the reasoning behind it.

## 2.1 The Core Principle: Five Surfaces, One Star

We use a **5-item bottom tab bar**, with the flagship feature (Replay) elevated to a center "star" position — physically larger, visually distinct, the way Instagram elevated the camera and the way every great app has one obvious hero action.

```
┌─────────────────────────────────────────────┐
│                                               │
│                 [ CONTENT ]                   │
│                                               │
├─────────────────────────────────────────────┤
│   Home    Timeline   ◉REPLAY   Stories   You  │
└─────────────────────────────────────────────┘
```

- **Home** — the daily emotional landing.
- **Timeline** — spatial/temporal exploration of everything.
- **◉ Replay** — the flagship, center, elevated. The "watch the movie of your life" button.
- **Stories** — curated AI-authored narrative collections.
- **You** — profile, insights, achievements, settings, and the AI Companion's home.

### Where did "Insights" and "Profile" go?

This is the consequential decision. The brief listed Insights and Profile as separate tabs. We **merge Insights into "You"** and **make the AI Companion accessible from everywhere** rather than living in a tab. Reasoning:

- **Insights is a destination, not a daily habit.** People check deep analytics weekly/monthly, not daily. Giving it a permanent tab wastes prime real estate and creates a "homework" tab people feel guilty about ignoring. It belongs *inside* "You," surfaced via the Home screen's snackable cards when something noteworthy is found. (Full Insights experience: Part 7.)
- **Profile in a self-app is "You,"** and it naturally absorbs identity, settings, achievements, and the analytics deep-dive.
- **The AI Companion must be omnipresent,** not buried in a tab. It lives as a **persistent, summonable orb** (detailed in Part 8) — swipe up from the tab bar, or tap the orb that appears contextually. Putting your most magical feature behind a tab is like hiding Siri in a folder.

The result: five surfaces, each earning its place in the daily-to-weekly rhythm, with the two most magical capabilities (Replay and the Companion) given special, non-standard treatment because they *are* special.

## 2.2 The Navigation Model

- **Bottom tab bar** for the five primary surfaces. Always glass, always floating slightly above the content (see Part 9 for the glass spec). It auto-hides on full-screen immersive experiences (any Replay, any full-screen Story, any single-memory view) so cinematic content is never framed by chrome.
- **The Companion orb** floats bottom-right on Home, Timeline, and Stories. It is suppressed during immersive playback (the Companion can be *summoned* there but isn't visually present, to protect the cinema).
- **Vertical depth, not horizontal sprawl.** Within each tab we go *deeper* (tap a card → expand → full screen) rather than adding more tabs. The mental model is "zoom in," consistent with the pinch-through-time gesture.
- **Back is always a downward/outward collapse.** Closing any expanded view animates it shrinking back into the card it came from (shared-element transition), so the user never loses their sense of place. No abrupt screen swaps.

## 2.3 Every Surface — Purpose, Why It Exists, What's On It

Below, each surface is specified at the IA level. Full screen-level design for the major ones follows in dedicated parts.

### 2.3.1 HOME — "What does my life want to show me today?"

**Purpose:** the daily emotional landing pad. The answer to "why open the app today."
**Why it exists:** the daily loop needs a home base that delivers value in 10 seconds and rewards 10 minutes. It is the retention engine.
**Contains:** Today's Memory (hero), This Day Last Year, Life Score, Growth Snapshot, Current Streaks, Mood/Fitness trends, Top Moments — all as a curated, scrollable, *finite* card stack that ends. (Full design: Part 3.)
**Refresh cadence:** the hero content rotates daily; the app is "new" every morning.

### 2.3.2 TIMELINE — "Show me everything, beautifully."

**Purpose:** the complete, navigable record of the user's life — the explorable map of all memories across all scales of time.
**Why it exists:** Home is curated *for* you; Timeline is where *you* take control and wander. Some sessions are about being shown; some are about searching, reliving a specific trip, finding a specific person. Timeline serves the second mode.
**Contains:** the zoomable time-fabric (life→decade→year→month→week→day), with photos, workouts, locations, notes, music, and achievements woven into a single continuous visual surface. (Full design: Part 4.)

### 2.3.3 ◉ REPLAY — "Watch the movie of my life."

**Purpose:** the flagship. Cinematic, narrated, auto-generated films of any time span.
**Why it exists:** this is the differentiated core — the thing no one else does. It converts data into emotion at the highest intensity. It is the center button because it is the product's soul.
**Contains:** Day / Week / Month / Year / Life replays, plus themed replays, the "director's controls," and the share pipeline. (Full design: Part 6.)

### 2.3.4 STORIES — "Read the chapters of who I am."

**Purpose:** AI-authored, longer-form narrative collections organized by *theme* rather than *time* — "My Fitness Journey," "My Relationship Story," "My Year 2026."
**Why it exists:** Replay is cinematic and time-bound; Stories are editorial and theme-bound. Humans understand themselves through stories with throughlines ("my career," "my health"), not just chronology. Stories is where the app becomes a *biographer*. It's also the most shareable, identity-affirming surface.
**Contains:** a shelf of generated Story collections, each openable as an immersive scroll-or-tap narrative. (Full design: Part 5.)

### 2.3.5 YOU — "Who am I, by the numbers and the arc?"

**Purpose:** identity, deep analytics (Insights), the Achievements vault, the Companion's home base, and all settings/privacy.
**Why it exists:** the user needs one place that is unambiguously *theirs* — their stats, their trophies, their controls, their relationship with the AI. It absorbs Profile + Insights + Settings to keep the tab bar lean.
**Contains:**
- **The identity header** — a living portrait (their most "them" photo), name, "life in numbers" ticker (days lived, memories held, places been).
- **Insights entry points** — Happiest Year, Most Productive Month, etc., as cards that open the full analytics experience (Part 7).
- **The Achievements vault** — collectible milestone cards (Part 1.3.3, Part 7).
- **The Companion** — full-screen conversation history with the AI (Part 8).
- **Settings & Privacy** — data sources, permissions, person-muting, export, delete-everything. Privacy is given first-class, beautiful treatment, not buried.

## 2.4 The Cross-Cutting Surfaces (Not Tabs, But Everywhere)

Three experiences are *modal/overlay* and accessible from anywhere, because they're contextual rather than destinations:

1. **The AI Companion** (summon from orb or swipe-up). Part 8.
2. **The Search/Ask field.** A single field at the top of Timeline and inside the Companion that accepts natural language ("show me last summer," "when was I happiest," "find photos with Mom"). Search *is* the Companion in input form — there is no separate "search engine" mental model; you just *ask your life questions.*
3. **The Share Composer.** Invoked from any memory, Replay, Story, or Insight. A unified, beautiful export/share pipeline (Part 10) — never a generic OS share sheet dump.

## 2.5 First-Run vs. Returning IA

The IA *adapts to data maturity*:

- **Day 0 (just onboarded):** Timeline, Insights, and Stories are thin. We *hide* what we can't fill well and lean almost entirely on Home + the Genesis Replay. Empty tabs are forbidden — a tab with nothing in it teaches the user the app is empty. Instead, sparse surfaces show "I'm still getting to know you — come back as I learn" states that are themselves beautiful and forward-looking.
- **Week 1–4:** surfaces progressively unlock with a small celebratory moment ("Your Timeline is ready," "I found enough to write your first Story"). Unlocking creates anticipation and teaches the app's scope gradually instead of overwhelming.
- **Month 3+ (mature):** all surfaces full; the app shifts from "showing you your past" to "narrating your ongoing life" — daily mood prompts, fresh weekly replays, evolving Story chapters.

This staged IA means the app feels *complete from day one* (because we hide thinness) while *growing more valuable over time* (because surfaces fill in), which is the ideal retention shape.

## 2.6 Information Architecture Map (Summary)

```
Life Replay AI
│
├── HOME  (daily emotional landing)
│     └─ card stack → expand any card → full memory/replay
│
├── TIMELINE  (zoomable life-fabric)
│     ├─ Ask field (natural-language search)
│     └─ pinch: life ⇄ decade ⇄ year ⇄ month ⇄ week ⇄ day
│
├── ◉ REPLAY  (flagship cinematic films)
│     ├─ Day / Week / Month / Year / Life
│     ├─ Themed replays
│     └─ Director controls + Share
│
├── STORIES  (AI-authored themed narratives)
│     └─ Story shelf → immersive narrative reader
│
└── YOU  (identity + insights + vault + companion + settings)
      ├─ Identity header (living portrait, life-in-numbers)
      ├─ Insights (full analytics, Part 7)
      ├─ Achievements vault
      ├─ Companion (conversation home, Part 8)
      └─ Settings & Privacy

Cross-cutting (no tab):
  • AI Companion orb (summon anywhere)
  • Ask / Search (natural language)
  • Share Composer (unified export)
```

---

# PART 3 — HOME SCREEN

Home is the most important screen in the product because it is the one users see most. It must deliver value in 10 seconds, reward 10 minutes, feel different every day, and never feel like a dashboard. This part specifies it completely.

## 3.1 The Governing Idea: "A Letter From Your Life"

Home is designed as if your own life wrote you a short letter this morning, choosing the few things it most wants you to see today. It is **curated, finite, and personal** — not an infinite feed. It scrolls to a definitive end. The emotional target of the *whole screen* is: *"My life is paying attention to me, and it's beautiful."*

Crucially, Home is **editorial, not exhaustive.** The AI editor picks today's story. Two users on the same day see completely different Homes. The same user sees a different Home tomorrow. This daily freshness, driven by a real editorial intelligence, is the core of the return habit.

## 3.2 The First 0.5 Seconds (Above The Fold)

What the user sees the instant Home loads, before any scroll:

1. **The ambient backdrop.** The entire screen background is a slow, living, depth-blurred crop of *today's hero memory* — barely moving (a 2% parallax drift), heavily darkened and blurred so text is legible. The room you're standing in is made of your own memory. This single decision makes Home feel alive and personal before you read a word.
2. **The greeting line.** Top-left, soft and small: *"Good morning, Maya."* Below it, the day's editorial subtitle — the AI's one-line "why you should care about today": *"A year ago, today was one of your happiest."* This is the hook line; it changes daily and is the single most A/B-tested string in the product.
3. **The hero card — "Today's Memory."** Occupying ~60% of the viewport. (Detailed in 3.3.) This is the payload. Even if the user does nothing else, this card alone justified the open.

There is **no tab bar visible until you scroll** (it fades in on first scroll), so the above-the-fold view is pure, uninterrupted emotion.

## 3.3 Section-By-Section Design

Home is a vertically scrolling stack of distinct, full-bleed-ish *modules*. The order is dynamic (the editor reorders by what's most compelling today), but the canonical set and design of each module:

### 3.3.1 Today's Memory (the hero)

**Purpose:** the single best emotional moment the app wants to show today.
**Emotional target:** instant warmth / nostalgia / delight.
**Layout:** a large rounded-rect card (28pt corner radius) filling most of the first screen. It is *not* a static photo — it's a **breathing memory**: a 3–5 second looping micro-clip (Ken Burns on a still, or a real Live Photo / video moment), with a subtle parallax. Overlaid at the bottom: a date stamp (*"July 14, 2025"*), a place (*"Lisbon, Portugal"*), and a one-line AI caption (*"The day you decided to stay an extra week."*).
**Interaction:**
- *Tap* → expands (shared-element zoom) into the full memory: all photos from that moment, the map, the workout if any, the music that was playing, who was there.
- *Hold* → the Hold-to-Replay: it begins playing as a mini-Replay under your finger.
- *Swipe up* on the card → launches the full Replay of that day.
- *Swipe left/right* on the hero → see *alternate* "today's memories" (the editor's 2nd and 3rd picks). A subtle dot indicator. This gives agency without clutter.
**Why it leads:** photos/faces are the highest emotional-density content we have. Lead with the strongest punch.

### 3.3.2 This Day Last Year (and "On This Day" stack)

**Purpose:** temporal anchoring — the most reliable nostalgia trigger we have.
**Emotional target:** nostalgia, the gentle vertigo of time passing.
**Layout:** a horizontally scrolling rail of "On This Day" cards — *1 year ago, 2 years ago, 5 years ago* — each a smaller memory card with the year badge prominent. The cards are color-graded progressively warmer/older as you scroll back, so time is *visible* in the palette.
**Interaction:** tap any → expand. The header line above the rail is editorial: *"On June 19th, across the years…"* A premium flourish: tapping "see all" stacks every June-19th in your history into a vertical "same day, every year" Replay — watching yourself age through a single calendar date is devastatingly powerful. (This specific feature tests as one of the most-shared in the product.)
**Edge case:** new users with <1 year of data → this section is replaced by "This Week" or "Your Earliest Memory" so it's never empty.

### 3.3.3 Life Score

**Purpose:** a single, glanceable, *gentle* read on how life is going lately.
**Emotional target:** self-awareness without judgment.

This is the most dangerous module in the app, so it gets the most careful design. A naive "score your life 73/100" is hostile, anxiety-inducing, and reductive. We redesign it entirely:

- **It is not a grade. It is a "weather report" for your life.** Visualized as a soft, abstract orb/aurora whose color and movement reflect a blended index of recent mood, sleep, activity, and social connection. Calm blue-greens = balanced; warm golds = thriving/energetic; muted greys = a low/quiet period (never "red/bad").
- **The number is secondary and optional.** Power users can enable a numeric index; by default we show a *qualitative phrase*: *"This week feels balanced."* / *"You've been quiet lately."* / *"You're on a roll."*
- **It always offers a door, never a verdict.** Tapping it doesn't show a report card — it opens "What's shaping this?" — the 3 factors most influencing the read, each tappable to the relevant trend, plus the Companion offering to talk about it.
- **It never shames.** A low period is framed with care and context: *"Things have been slower lately. Last time this happened, March, it turned around. Want to look back?"* The Life Score is a compassionate mirror, not a judge.

**Why it exists despite the risk:** a single living indicator of "how am I, really?" is profoundly valuable and nothing else provides it. Done with cruelty it's a churn machine; done with compassion it's a reason to return daily.

### 3.3.4 Growth Snapshot

**Purpose:** make personal growth legible at a glance.
**Emotional target:** quiet pride, momentum.
**Layout:** a compact "then → now" card. One rotating dimension per day, chosen by the editor for where the user has a compelling delta: *"A year ago: 8,000 steps/day. Now: 11,400."* with a small rising-line sparkline morphing between the two states on appearance. The visual motif is the **arc** (rising path).
**Interaction:** tap → opens the full growth comparison for that dimension (overlaid charts, the narrative arc the AI detected). Swipe → cycle dimensions (fitness, sleep, reading, travel, social, finance).
**Tone rule:** always self-vs-self, always framed as gain. If a metric declined, the editor either skips it or frames it with compassion and context, never as failure.

### 3.3.5 Current Streaks

**Purpose:** the *floor* of the retention model — the obligatory habit layer, kept tasteful.
**Emotional target:** light achievement, continuity.
**Layout:** a slim horizontal row of streak "embers" — small glowing flame/ring icons with counts: *journaling 14 days, movement 6 days, app-open 30 days.* They glow brighter the longer the streak; a streak about to break has a subtle dimming pulse (gentle, never alarmist).
**Interaction:** tap → streak detail with the calendar of kept days and a "don't break it" gentle nudge.
**Design discipline:** streaks are deliberately *understated* — one slim row, not a screen. We refuse to let the product become a streak-anxiety machine. Streaks are the seatbelt, not the engine. The engine is emotion. (See Part 12 for the self-critique on this exact risk.)

### 3.3.6 Mood Trends

**Purpose:** reflect emotional patterns over time.
**Emotional target:** self-understanding, curiosity.
**Layout:** a soft, flowing area-graph (more "aurora ribbon" than "stock chart") of mood over the last 30 days, derived from end-of-day check-ins + inferred signals (activity, social, sleep, photo sentiment). Annotated with 1–2 AI callouts: *"Your best stretch was the week you were in the mountains."*
**Interaction:** tap → full mood analytics in Insights (Part 7); tap a callout → jump to that memory.

### 3.3.7 Fitness Trends

**Purpose:** surface the body's story — effort, movement, recovery.
**Emotional target:** achievement, momentum, care for self.
**Layout:** a glanceable trio of living rings/bars (movement, workouts, sleep) with a one-line headline: *"Strongest week in 3 months."* We borrow the legibility of Apple's activity rings but render them in our warmer, cinematic material language, and we *narrate* them.
**Interaction:** tap → fitness deep-dive (Part 7), including "strongest fitness period" and PRs.

### 3.3.8 Top Moments

**Purpose:** a curated rail of recent peaks — the highlights the editor thinks deserve a second look.
**Emotional target:** happiness, pride, a "good life" feeling.
**Layout:** a horizontally scrolling rail of medium memory cards, each a breathing micro-clip, spanning the last ~30 days, ranked by the app's "moment significance" score (emotional density, rarity, social presence, user engagement).
**Interaction:** tap → expand; the whole rail can be played as a "Month so far" mini-Replay via a play button on the section header.

### 3.3.9 The Closer ("That's all for today")

**Purpose:** architect the end-on-a-high (Law 5). Home is finite; it must end with intention.
**Layout:** at the bottom of the scroll, a calm, full-width closing card: a single beautiful line — *"That's your life today, Maya. I'll find something new for tomorrow."* — over a soft animated gradient. Below it, one gentle forward hook: either the evening reflection prompt ("How was today?") or a teaser ("Your 2026 Year Replay unlocks in 12 days").
**Why it matters:** infinite feeds end in emptiness and self-loathing. A finite, well-closed Home ends in fullness and anticipation. This is a core differentiator from every doomscroll product.

## 3.4 The Editorial Engine (Why Home Feels Alive)

Home is only as magical as the intelligence that curates it. The design depends on an **editorial ranking system** with these inputs:

- **Recency × Rarity** — recent peaks and rare events rank high.
- **Emotional density** — faces, smiles, novel locations, milestone events.
- **Temporal resonance** — "on this day" matches, anniversaries (positive ones).
- **Freshness/anti-repetition** — never show the same hero twice in a short window; deliberately resurface forgotten content.
- **Mood-awareness** — if recent signals suggest a low period, the editor weights toward comforting, uplifting, agency-restoring content (and engages the emotional-safety system).
- **Engagement learning** — what this specific user lingers on, replays, and shares teaches the editor their taste.

The design implication: every module is *optional and reorderable.* Home is a *layout system*, not a fixed template. Some days the hero is a workout PR; some days it's a face; some days it leads with an Insight ("This was your most-traveled month ever"). This variability, governed by genuine intelligence, is why it never gets stale.

## 3.5 Home — States & Edge Cases

- **First-run / sparse data:** Home leans on the Genesis Replay's afterglow + "This Day"/"Earliest Memory" + a warm "I'm still learning you" closer. No empty modules — modules that can't be filled well are simply absent today.
- **Heavy/grief content present:** the editor demotes anything flagged by the emotional-safety system; the gentle gate (Part 1.5) governs any sensitive surfacing.
- **Loading:** never a spinner over a blank screen. The ambient backdrop and greeting load first (cached); cards fill in with a soft staggered fade + skeleton shimmer in our material language.
- **Offline:** cached hero + last-known modules render; live-computed modules (Life Score) show last value with a subtle "as of yesterday" note.
- **Power user (months of data, daily check-ins):** Home gets richer callouts, deeper "on this day" stacks, and earlier access to long-range Replays.
- **The "nothing happened today" day:** the app never says "no memories." A quiet day is reframed: *"A calm one today. Here's a good one from before."* Quiet is a valid texture of life, treated with the same reverence as a peak.

---

# PART 4 — TIMELINE EXPERIENCE

The brief is explicit: "Not a boring list." A vertical list of dates is what every photo app already does and it is where memories go to be ignored. The Timeline must be a *place* you want to wander, a spatial representation of time that feels like exploring a galaxy of your own life. This part designs that.

## 4.1 The Core Metaphor: The Living River of Time

We reject the **list** and the **grid** as primary metaphors. Instead, the Timeline is **a continuous, flowing "river of time"** — a single vertical ribbon that you travel along, where time flows top (past) to bottom (now), and where the *width, color, density, and texture* of the river encode the shape of your life.

Imagine a river seen from above that you fly along:

- **Where life was eventful**, the river is *wide, bright, dense* with memory-nodes clustered close.
- **Where life was quiet**, the river is *narrow, calm, sparse*.
- **The color of the water** shifts with your mood/season trends — warm gold in thriving stretches, cool blue in quiet ones.
- **Tributaries** flow in where major life threads begin (a relationship starts, you move cities, you take up running) and out where they end.

This means **the shape of your life is visible before you read a single label.** You can see, at a glance, your peaks and valleys, your busy years and your fallow ones. No list can do that. This is the unique, ownable Timeline metaphor.

## 4.2 The Signature Interaction: Pinch-Through-Time (Temporal Zoom)

The Timeline has one transcendent interaction that ties all scales together: **pinching changes temporal resolution**, continuously and fluidly, across five levels. This is the gesture that makes the Timeline feel unlike anything else.

```
   pinch OUT (zoom to overview)              pinch IN (zoom to detail)
   ◀──────────────────────────────────────────────────────────────▶
   LIFE        DECADE        YEAR        MONTH        WEEK        DAY
  (galaxy)   (constellations) (river)  (stream)    (pools)    (a single drop)
```

The transitions are *continuous*, not discrete tab-switches — nodes smoothly grow, separate, and resolve into more detail as you pinch in, and merge, shrink, and abstract as you pinch out. It feels like Google Earth for your life: one seamless zoom from the whole planet of your existence down to a single afternoon. The current scale is shown by an unobtrusive readout that updates live.

### 4.2.1 LIFE scale — "The Galaxy"

**Purpose:** see your entire life at once.
**Visual:** the whole river compressed into a single vertical aurora from birth (or earliest data) to now. Major **eras** are auto-detected and labeled in large, cinematic type floating beside the river: *"Childhood," "The College Years," "The London Era," "Becoming a Parent."* (Era detection is an AI feature — it finds the structural breaks in your life: moves, job changes, relationship shifts, major routine changes.) Brightness pulses mark the few most significant moments of your entire life.
**Interaction:** tap an era label → smoothly zoom into that era. This is the "10,000-foot view" that makes people gasp — *"that's my whole life on one screen."*

### 4.2.2 DECADE scale — "Constellations"

**Purpose:** see a span of years as related clusters.
**Visual:** years rendered as nodes of varying size (size = density of memories/significance), connected by the flowing river, with seasonal color banding. Recurring threads (a person, a hobby, a city) appear as colored strands weaving through multiple years.
**Interaction:** tap a year → zoom to year.

### 4.2.3 YEAR scale — "The River" (the default landing)

**Purpose:** the primary working view — one year as a flowing, scrollable ribbon.
**Visual:** twelve months flow vertically. Each month's segment width/brightness reflects its activity. Memory-nodes (photo thumbnails, workout glyphs, location pins, note marks, achievement badges, music notes) float *along* the river at their dates, sized by significance. Major moments "bloom" larger. Season is encoded in the ambient color grade behind the river.
**Interaction:** scroll to travel through the year; tap any node to expand; pinch to change scale; tap a month label to zoom to month.

### 4.2.4 MONTH scale — "The Stream"

**Purpose:** a month in navigable detail.
**Visual:** weeks as gentle bends in the stream; days as stepping-stones. Now individual memory thumbnails are legible. Workouts show as small effort-glyphs whose size = intensity; locations cluster on a tiny inline map ribbon along the bank.
**Interaction:** tap a day → zoom to day; horizontal swipe → adjacent months.

### 4.2.5 WEEK scale — "The Pools"

**Purpose:** a week's rhythm — the rhythm of a life is most legible at the week.
**Visual:** seven day-pools, each showing its texture: a morning run, a lunch photo, an evening with friends, a late bedtime. This is where daily *patterns* become visible (you always run Tuesdays; weekends are social). The AI annotates rhythm: *"Your most active week this month."*

### 4.2.6 DAY scale — "A Single Drop"

**Purpose:** one day, fully reconstructed.
**Visual:** the richest, most cinematic single-unit view — a vertical day-story. The day is reconstructed as a sequence: where you woke, what you did, the photos in order, the workout with its route on a map, the music you played, the weather, who you were with, the note you wrote, when you slept. It reads like a **page from a beautifully designed diary you didn't know you were keeping.**
**Interaction:** the day can be *played* as a Day Replay (one tap to the flagship experience, Part 6); each element is tappable for detail; swipe left/right for adjacent days.

## 4.3 Weaving The Data Types Into One Surface

The brief asks how photos, workouts, locations, notes, and achievements combine. The answer: **they are not separate layers you toggle — they are different kinds of stones in the same river,** unified by a single visual language and woven by time and place.

- **Photos/videos** — the primary nodes; breathing thumbnails, sized by significance.
- **Workouts** — *effort-glyphs*: a luminous stroke whose length = duration, thickness = intensity, color = type (run/lift/yoga/cycle). A workout with a GPS route renders its route shape *as* the glyph — your morning run becomes a small piece of map-art on the river.
- **Locations** — the river itself bends and is color-tinted by *place*; significant locations drop a pin with a one-word label. Travel shows as the river briefly leaving its banks and flowing somewhere new (a strong visual signal for "you went somewhere").
- **Notes / journal / mood** — small handwritten-style marks on the bank; tapping reveals your own words, in the memory serif typeface, treated as precious.
- **Music** — faint note-glyphs that, when the day/era is played, become the actual soundtrack. The song you played most that summer *is* the summer's theme.
- **Achievements** — embossed metallic badge-nodes that sit slightly *above* the river surface (they're earned, they float), catching light. (Detailed in Part 7.)

**The unifying rule:** every data type answers to the same physics (flow, light, depth, significance-sizing) so the Timeline reads as *one organism*, not a pile of integrations. A workout, a photo, and a journal entry from the same afternoon visually *belong together* because they share the same stretch of river.

### 4.3.1 Layer focus (not layer toggles)

Rather than checkboxes ("show workouts ☑"), the user can *focus* a thread by tapping its strand at the decade/year scale — e.g., tap the "running" strand and the river de-emphasizes everything else, letting the user trace their entire running history as a glowing line through years. This is exploration-as-storytelling, and it directly feeds Stories (Part 5) and Insights (Part 7).

## 4.4 The Ask Field (Natural-Language Navigation)

At the top of Timeline floats the **Ask field** (the Companion in input form): *"show me last summer," "find the trip to Japan," "when did I start lifting," "photos with Dad."* Results don't dump as a grid — they *fly you* to that stretch of river with a smooth camera move and highlight the matching nodes. Search is travel, not a results page. This makes the entire timeline addressable by memory and language, which is how humans actually recall ("that time we…"), not by date.

## 4.5 Timeline — Motion & Feel

- **Inertial, weighted scrolling** — the river has mass; flicking sends you gliding with natural deceleration. Time should feel like it has momentum.
- **Parallax depth** — nodes nearer "the surface" move faster than the deep riverbed, creating real 3D depth. The Timeline is a space, not a page.
- **Light responds to attention** — the node under your gaze/center subtly brightens and the soundtrack swells faintly; moving away dims it. The Timeline breathes around your focus.
- **Haptics as texture** — a soft tick as each month boundary passes under the centerline; a richer thunk when a major moment crosses center. You can almost *feel* time passing.
- **Audio (optional, on by default with sound)** — a low ambient hum that pitches subtly with era; the music-glyphs whisper their songs as you pass. Muting is one tap; the experience is complete silent too.

## 4.6 Timeline — States & Edge Cases

- **Sparse history:** a short river is still beautiful — we never pad it. A 3-month-old account shows a small, jewel-like stream with an inviting "this will grow with you" headwater at the top. We lean into *potential* rather than apologizing for thinness.
- **Huge libraries (100k+ photos):** significance-ranking and clustering keep the river legible — we never render 100k nodes; we render the *meaningful* ones at each scale and resolve more on zoom (level-of-detail rendering). Performance budget: 60fps scroll/zoom is non-negotiable; this is a flagship surface and jank would shatter the "premium" promise.
- **Data gaps (phone lost, account paused):** gaps are rendered honestly but gently — the river narrows to a quiet thread labeled softly, never an alarming "NO DATA." Absence is part of a life too.
- **Privacy / muted people:** muted-person memories are excluded from the river until unmuted; sensitive clusters obey the gentle gate.
- **First time opening Timeline:** a 4-second guided fly-through (skippable) zooms from LIFE scale down to today, teaching the pinch-through-time gesture *by performing it*, then hands control to the user at the YEAR scale. We teach the gesture by showing its payoff, not with a coachmark.

---

# PART 5 — STORIES EXPERIENCE

If Replay (Part 6) is the *cinema* of your life, Stories is the *literature* of your life. Stories are AI-authored, theme-based narrative collections — "My Fitness Journey," "My College Life," "My Relationship Story," "My Career Growth," "My Year 2026." This part designs how they're generated, structured, and presented.

## 5.1 What A Story Is (And Isn't)

A Story is a **curated, authored narrative around a single throughline of your life**, assembled from your memories and told with a beginning, a middle, and a meaning. It is *not* a chronological dump and *not* a photo album. The defining quality is **authorship**: the AI acts as a biographer who has read your entire life and decided to tell *this* thread *well.*

The brief asks: Instagram Stories? Netflix documentary? Interactive timeline? The answer is **a new format that borrows the best of all three** and is none of them exactly:

- From **Instagram Stories**: the intimate, full-screen, tap-to-advance, ephemeral-feeling pacing and the vertical format.
- From **Netflix documentaries**: the narrative arc, chapters, narration, score, and the feeling of "this was *produced.*"
- From **interactive timelines**: the ability to branch, expand, and explore rather than passively watch.

We call the format **"Chapters"** — a hybrid of cinematic Story-card pacing with documentary narration and optional interactive depth.

## 5.2 How Stories Are Generated

Stories are generated by the **Biographer engine**, which works in three passes:

1. **Thread detection.** The engine scans the user's life-graph for coherent throughlines: recurring people (→ relationship stories), recurring activities (→ fitness/hobby journeys), location arcs (→ "your years in Berlin"), temporal spans (→ "Your 2026"), and milestone chains (→ "career growth"). Each candidate thread is scored for *narrative strength* (does it have an arc? a beginning, change, and a now?).
2. **Arc construction.** For each strong thread, the Biographer builds a **dramatic structure**: the origin ("where it began"), the rising action (the build, the work, the setbacks), the turning points (the moments that changed things), and the present ("where you are now"). It selects the *fewest, strongest* memories to tell that arc — editing is the art. A 4-year fitness journey might become 9 beats, not 900 photos.
3. **Voice & scoring.** The Biographer writes the narration in the product's warm, literary voice, selects a musical score that matches the arc's emotional shape, chooses the color grade and pacing, and assembles the chapter sequence.

**Critical design principle: Stories are *proposed*, not just *generated and hidden.*** The app proactively surfaces a new Story when it has enough material: *"I think I've understood your running journey well enough to tell it. Want to see?"* This is a magical moment — the app announcing it has *understood something about you.* The proposal itself is a retention and emotion event.

### 5.2.1 Story types (the starter set)

- **Time-bound:** "My Year 2026," "My Summer," "This Decade."
- **Relationship:** "Me & Sarah" (per significant person), "My Friends," "Becoming a Parent."
- **Body/Health:** "My Fitness Journey," "The Year I Got Strong," "My Sleep Story."
- **Place:** "My Years in [city]," "Everywhere I've Been."
- **Pursuit/Career:** "My Career Growth," "Learning Guitar," "My Reading Life."
- **Growth/Identity:** "How I've Changed," "The Hard Year," "Becoming Myself."
- **User-requested:** the user can ask the Companion to author any Story — *"Tell the story of my relationship with my mom"* — and the Biographer composes it on demand.

## 5.3 The Stories Surface (The Shelf)

The Stories tab opens to **The Shelf** — a beautiful, editorial library of the user's Stories.

**Layout:** not a grid of equal tiles (that's a CMS). Instead, a **magazine-cover treatment** — each Story is a tall, rich "cover" with a hero image, an evocative title in display type, a subtitle (*"4 years · 9 chapters"*), and a living micro-loop. Featured/new Stories get full-width hero placement; older ones flow into a secondary rail. It feels like the cover wall of a magazine *about you.*

**Sections of the Shelf:**
- **"New from your Biographer"** — freshly proposed Stories, badged, top of shelf.
- **"Your Stories"** — everything authored, sorted by recency/significance.
- **"Chapters in progress"** — ongoing threads ("My Year 2026" updates as the year unfolds; "My Fitness Journey" gains chapters as you keep training). These show a subtle "still being written" shimmer — your life is ongoing, so are its stories.
- **"Ask for a Story"** — an entry point to request any Story from the Companion.

## 5.4 The Reader (Inside A Story)

Tapping a Story cover opens **The Reader** — the immersive narrative experience. This is where the Chapters format lives.

**Open:** the cover expands full-screen (shared-element), the score fades in, and a title sequence plays — the Story's title in display type over the hero, like the cold open of a documentary. ~3 seconds, skippable by tap.

**Structure:** the Story is a sequence of **chapters**, each chapter a sequence of **beats** (cards). The default experience is **auto-playing with narration** (like a documentary), but the user controls pacing:

- **Auto mode (default):** beats advance themselves at a reading/viewing pace, narration plays (text always; voice optional), score swells and resolves across chapters. The user can just *watch.* This is the "Netflix" mode.
- **Tap mode:** tap right to advance, left to go back (the "Instagram Stories" muscle memory). Auto-advance pauses the moment the user takes control.
- **Explore mode:** any beat can be *expanded* — pull down on a beat to "step inside" it: see all the photos from that moment, the map, the full journal entry, the workout. This is the "interactive timeline" depth. Release to return to the narrative flow exactly where you left it.

**Beat anatomy (a single card):**
- Full-bleed breathing media (photo/video/route-art).
- A line or two of narration in the literary voice, beautifully set, entering with a gentle typographic animation.
- A subtle date/place/context stamp.
- The score underneath, matched to the beat's emotional weight.
- Optional "step inside" affordance for depth.

**Chapter breaks:** between chapters, a full-screen title card with the chapter name (*"Chapter 3 — The Setback"*) and a breath of near-silence, resetting the emotional pacing. Chapters give the Story *shape* and make a long life-thread digestible.

**The ending:** every Story resolves with a **reflection beat** — the Biographer's closing thought (*"You started running to lose weight. Somewhere in year two, it became how you think. You're not chasing anything anymore — you just go."*) followed by a single forward line (*"And you're still writing this one."*). Then the share/keep affordances. End-on-a-high, always.

## 5.5 Why Stories Look The Way They Do (vs. the alternatives)

- **Why not just Instagram Stories?** IG Stories have no *arc* — they're a chronological string with no meaning imposed. Our differentiation is *authorship and narrative.* We keep IG's intimate full-screen pacing but add the spine of a real story.
- **Why not pure Netflix documentary (passive video)?** Passive video can't be *explored*, and rendering bespoke video for every thread is expensive and rigid. Our card-based Chapters format gives documentary feel *plus* interactivity *plus* the ability to regenerate/update cheaply as life continues.
- **Why not a plain interactive timeline?** A timeline has no *editing* — no point of view. The whole value of a Story is that the Biographer *chose* what matters and what to leave out. Curation is the product.

The Chapters format is the synthesis: **the soul of a documentary, the intimacy of Stories, the depth of a timeline.**

## 5.6 Stories — Living & Evolving

Stories are not static exports. They are **living documents**:

- Ongoing threads gain chapters automatically ("My Year 2026" writes itself as the year passes; the user gets a gentle "a new chapter was added" moment).
- The Biographer can *revise*: if it learns more (you tag a person, you add context), it can re-edit a Story for the better and tell you it did.
- The user can **co-edit**: reorder beats, swap a photo, tweak a narration line, or tell the Companion "this part is wrong, it was actually about X" — and the Story updates. Co-authorship deepens ownership and emotional attachment. The Story becomes *ours*, not just the machine's.

## 5.7 Stories — States & Edge Cases

- **Not enough data for a strong Story:** we *don't* generate a weak one. A bad Story damages trust more than a missing one. The Biographer waits and the Shelf shows "Stories are being written as your life unfolds" with 1–2 teasers of threads it's watching.
- **Sensitive threads (a breakup, a loss):** these *can* make the most powerful Stories, but they're never auto-published. The Biographer asks: *"There's a hard, important story here about [thread]. I can tell it gently, whenever you're ready."* The user opts in; tone shifts to careful reverence; the emotional-safety system governs throughout.
- **Factual errors in inference:** every Story has a quiet "something's not right?" affordance; corrections improve the underlying life-graph everywhere, not just the Story. We treat the user as the ultimate authority on their own life.
- **Sharing:** Stories are highly shareable (Part 10) — but a private "step inside" depth is never included in a share; only the curated, user-approved beats export. Privacy by default in every share.

---

# PART 6 — REPLAY EXPERIENCE (THE FLAGSHIP)

This is the soul of the product — "the Netflix of your life." Replay turns any span of time into a cinematic, narrated, scored film, generated automatically and watchable in one tap. It is the center button. It is what people will describe to their friends. This part designs it exhaustively.

## 6.1 The Promise

> **"Press play on any part of your life, and watch it as a movie."**

A Replay is not a slideshow. A slideshow is photos with a transition. A Replay is a **directed film** with: an opening, an arc, a score that rises and falls with the emotional content, narration that gives meaning, editing rhythm matched to the music, color grading matched to the era, and an ending that resolves. The difference between a slideshow and a Replay is the difference between a folder of photos and *Boyhood.*

## 6.2 The Replay Surface (The "Theater")

The Replay tab opens into **The Theater** — a dark, cinematic, premium space (true black `#000`, the only place in the app we go fully black, because cinema demands it). It is laid out like a streaming service's home, but every title is *you.*

**Top — The Marquee.** A large, auto-playing hero Replay the app most wants you to watch right now — usually the freshest compelling one: *"Last Week"* or *"This Day, Every Year"* or a newly-unlocked *"2026 So Far."* A big glowing **▶ Play** and a one-line pitch (*"7 days. 1 unforgettable weekend."*).

**Below — The Rows (Netflix-style shelves), but emotionally curated:**
- **"Made for you today"** — the editor's fresh picks.
- **"Your Days"** — recent Day Replays.
- **"Your Weeks" / "Your Months"** — rolling spans.
- **"The Years"** — one cover per year, aging backward — a powerful row to scroll.
- **"Themed Replays"** — "Every sunset you've photographed," "All your finish lines," "Nights out," "Mornings," "Faces of [person]." (These are the magic — see 6.5.)
- **"Continue watching"** — Replays you paused.

**The crown — "Life Replay."** A single, special, full-width cinematic tile at the bottom, treated with the most reverence in the entire app: *"Your Life. The whole story."* It is partially locked/gated for new users (you earn the full Life Replay as your data deepens), which makes it aspirational. Tapping it is the single most emotional action in the product. (See 6.4.5.)

## 6.3 The Player (Watching A Replay)

The Player is the most cinematic screen we build. Design specs:

**Entry:** tapping Play does a *theater dim* — the surrounding UI darkens and recedes, the tile expands to full screen, a beat of black, then the film opens. This 800ms ritual signals "something is about to begin." Anticipation is part of the experience.

**During playback:**
- **Full-screen, chrome-free.** No tab bar, no buttons — pure film. Controls appear on tap and auto-hide in 2s.
- **The opening title.** Every Replay opens with a title card in display type: *"Last Week"* / *"July 2025"* / *"2026."* Establishes it as a *work*, not a feed.
- **Directed editing.** Shots are cut to the music's rhythm; emotional peaks get longer holds, montages get rapid cuts. Ken Burns moves on stills are *motivated* (push in on a face, pull out to reveal a landscape), never random drift.
- **Narration.** Sparse, well-placed lines in the warm literary voice — on-screen text always, optional AI voice-over (multiple voice options, including a calm default). Narration gives *meaning*: *"This was the week everything sped up."*
- **The score.** Adaptive music that matches the arc. (Licensed library + AI-assisted scoring; the user's *own* most-played track of that era can optionally become the theme — devastating in the best way.)
- **Color & grain.** Era-matched grading (warmer/grainier for older spans).
- **Live captions of context** — subtle lower-third stamps: date, place, "your 300th run," etc., appearing and dissolving like a tasteful documentary.

**Scrubbing & control:**
- **Tap** → toggle controls (play/pause, a beautiful timeline scrubber, the director button, share, captions/voice toggles).
- **The scrubber is a filmstrip** of the actual frames — scrubbing flies through your own memories.
- **Hold left/right edges** → rewind/fast-forward with a film-reel whir.
- **Swipe down** → exit (the film collapses gracefully back into its tile; never a hard cut to black).
- **Double-tap a moment** → "save this moment" / "tell me about this" (Companion hook).

**The ending:** the score resolves, a closing card (*"That was your week, Maya."*), then a gentle **end-screen** with three choices, always in this order: **Share** (Part 10), **Watch another** (autoplay queue of related Replays — the "binge" hook, used tastefully), and **Reflect** (one-line journaling prompt tied to what you watched). End-on-a-high with a forward door.

## 6.4 The Five Spans

The brief specifies Day, Week, Month, Year, Life. Each has a distinct *length, structure, and emotional intent* — they are not the same template at different durations.

### 6.4.1 Day Replay (~20–40 sec)

**Intent:** intimacy. The texture of a single day.
**Structure:** chronological micro-film — morning to night. Gentle, diary-like. Best generated for *eventful* days; for quiet days it leans poetic and short (*"A quiet Tuesday"*). Accessible in one tap from any day in Timeline or from the evening reflection. The Day Replay is the *habitual* Replay — small, frequent, low-stakes, the daily dessert.

### 6.4.2 Week Replay (~40–70 sec)

**Intent:** rhythm. The shape of your week — work and rest, effort and reward.
**Structure:** themed by the week's dominant texture (a "big weekend" week vs. a "heads-down" week gets different treatment). Auto-generated every Sunday evening as a gentle ritual: *"Your week is ready."* This is a key weekly retention beat — a standing appointment with yourself.

### 6.4.3 Month Replay (~60–90 sec)

**Intent:** progress. What this month *added up to.*
**Structure:** three acts — how it began, what built, where it landed. Surfaces the month's milestones, its most-photographed person, its trips, its PRs. Delivered as a monthly ritual ("September, in review").

### 6.4.4 Year Replay (~2–4 min) — the "Wrapped" moment

**Intent:** awe and identity. The Spotify-Wrapped-grade event, but cinematic and personal.
**Structure:** a full short film with chapters (seasons or detected eras within the year), a real narrative arc, statistical reveals woven in cinematically (*"You traveled 14,000 miles." "You met 40 new faces." "Your word of the year was 'again.'"*), and a triumphant resolve. Released as a **massive annual moment** (see Part 10 — this is our virality supernova). The Year Replay is *the* shareable artifact.

### 6.4.5 Life Replay (~5–8 min) — the crown jewel

**Intent:** transcendence. The whole arc of a human life, told as a film. This is the feature people will cry at.
**Structure:** the Biographer's masterwork — eras as chapters (*"Childhood," "Becoming," "The Building Years," "Now"*), the recurring people who shaped you appearing and reappearing across decades, the throughlines (a city, a craft, a love) traced from start to present, scored like a film, narrated with genuine literary weight. It ends not in the past but pointed at the future: *"And this is only the part you've lived so far."*

**Why it's gated for new users:** the Life Replay is only as powerful as the data behind it. We don't cheapen it with a thin version. New users see it as a locked, glowing, aspirational tile — *"Your Life Replay is being written. Keep living; it gets more beautiful every day."* Earning it over time makes it sacred and gives a long-horizon retention goal nothing else provides. (Premium users can generate it earlier / in higher fidelity — Part 11.)

## 6.5 Themed & On-Demand Replays (The Surprise Engine)

Beyond time-spans, the magic is **thematic Replays** that cut *across* time:

- **"Every sunset you've ever photographed"** — set to one continuous track. Quietly stunning.
- **"All your finish lines"** — every race, every PR, every summit.
- **"[Person], over the years"** — a single relationship as a film.
- **"Your mornings" / "Your nights out" / "Your hometown."**
- **"The places that became home."**

These are generated proactively (surfacing as "Made for you today") and on demand via the Companion: *"Make me a Replay of all my time near the ocean."* The combinatorial surprise of themed Replays is a near-infinite source of fresh wow — the app can always show you a film of yourself you've never seen.

## 6.6 The Director (Light-Touch Control)

Replays are auto-directed (that's the magic — zero effort), but a **Director panel** (pull up during/after a Replay) offers tasteful control without turning this into iMovie:

- **Mood/length presets:** "Shorter," "More upbeat," "More reflective," "More cinematic."
- **Soundtrack:** swap the score; "use my music"; pick a mood.
- **Voice:** narration on/off; voice selection; "less narration."
- **Include/exclude:** mute a person, exclude a place, focus a theme.
- **Re-cut:** "make it again" — regenerates a fresh edit (no two cuts identical; re-rolling is itself fun).

Design discipline: the defaults must be *so good* that 95% of users never open the Director. Control is for the power user and for fixing the rare miss — never a required step. The product directs; the user merely nudges.

## 6.7 Replay — Motion, Sound & Craft

- **The dim-and-open ritual** (800ms) before every Replay — the curtain.
- **Frame-accurate music sync** — cuts land on beats; this single quality is what separates "premium" from "PowerPoint."
- **Motivated camera moves** on stills — every push/pull means something.
- **Haptic accents** — a soft pulse on title cards and emotional peaks (subtle; can be disabled).
- **Graceful collapse on exit** — never a jarring stop; the film always folds back into where it came from.
- **Letterboxing as a feature** — subtle cinematic bars during the most filmic moments to signal "this is a movie," released for full-bleed immersive beats.

## 6.8 Replay — States & Edge Cases

- **Generating:** Replays render fast, but when one needs a beat, we show the *gathering* animation from onboarding (memories swirling), never a progress bar. Waiting is reframed as "the film is being assembled." Most common spans are pre-generated in the background so Play is instant.
- **Thin spans (a near-empty week):** we don't force a film. We offer a short poetic micro-Replay or gently suggest a richer span: *"This week was quiet — want to watch the month instead?"*
- **Sensitive content:** never auto-included in a Replay without the gentle gate. A grief-related Life Replay chapter is opt-in and handled with reverence.
- **Offline:** previously generated Replays are cached and fully watchable offline; new generation queues until reconnect with a clear, calm status.
- **Performance:** playback must be buttery (60fps, no stutter on transitions, instant scrub). A janky Replay destroys the entire premium thesis — this is the highest-priority performance budget in the app.
- **Accessibility:** every Replay has full captions; narration text is always present (voice optional); reduced-motion mode swaps parallax/Ken-Burns for gentle cross-dissolves while preserving the narrative; full VoiceOver descriptions of each beat.

---

# PART 7 — INSIGHTS EXPERIENCE

Insights is the analytical brain of the product — "Happiest Year," "Most Productive Month," "Strongest Fitness Period," "Best Sleep Streak," "Most Travelled Year," "Most Social Year," "Most Growth Year." The danger is obvious: analytics dashboards are where emotion goes to die. This part designs analytics that *feel* — charts that are beautiful, reports that read like revelations, and a visual language that turns data into story. Insights lives inside the **You** tab.

## 7.1 The Governing Idea: "Superlatives, Not Spreadsheets"

Humans don't think in line charts; they think in *superlatives and stories.* "My happiest year." "The strongest I've ever been." "The year everything changed." So Insights leads with **the superlative as the headline** and uses the chart as *evidence and exploration*, never as the opening move (Law 1).

Every Insight is structured as:
1. **The headline** — a superlative, in big beautiful display type: *"2024 was your happiest year."*
2. **The proof** — one elegant, glanceable visualization that makes the claim obviously true.
3. **The why** — the AI's interpretation: *"You traveled more, slept more, and saw the people you love most weeks in a row."*
4. **The door** — tap to explore deeper, compare years, or ask the Companion about it.

This turns analytics into a series of *small revelations about yourself*, which is curiosity and growth fuel, not homework.

## 7.2 The Insights Surface

Inside **You → Insights**, the layout is a **gallery of "Life Awards"** — each a rich card announcing a superlative, plus deeper analytical "Labs" for users who want to dig.

**Section A — "Your Life in Superlatives" (the headline gallery):**
A scrollable set of award cards, each beautiful enough to screenshot:
- **Happiest Year** — with the mood-aurora of that year.
- **Most Productive Month** — output/achievement density.
- **Strongest Fitness Period** — peak training block.
- **Best Sleep Streak** — longest run of good sleep.
- **Most Travelled Year** — a glowing globe with your routes.
- **Most Social Year** — the year of the most people and gatherings.
- **Most Growth Year** — the year of greatest positive change across dimensions.

Each card is tappable into a full report (7.4) and shareable (Part 10).

**Section B — "The Labs" (explorable analytics):**
For users who want depth — dimension-by-dimension explorers (Mood, Sleep, Fitness, Travel, Social, Focus/Productivity, Finance-milestones, Reading/Learning). Each Lab is a beautiful, interactive deep-dive (7.3). These are *opt-in depth*, never forced.

**Section C — "Ask your data" — a direct line to the Companion** for any analytical question (Part 8).

## 7.3 Designing The Visualizations (Charts With A Soul)

We reject default chart-library aesthetics entirely. Every visualization obeys the design system (Part 9) and these rules:

- **Organic over rigid.** Mood and wellbeing data render as **flowing aurora ribbons / gradients**, not bar charts. Continuous emotional data deserves continuous, soft forms.
- **Embodied metaphors.** Fitness uses **living rings and effort-glyphs**; travel uses a **glowing 3D globe with arcs**; sleep uses a **night-sky band** (deeper blue = deeper sleep, stars = dreams/REM); social uses a **constellation of people** (nodes = people, brightness = closeness/recency, lines = shared moments).
- **Always annotated by the AI.** No chart ships without at least one human-language callout pinned to its most interesting point: *"This spike was the month you moved."* A chart without narration is a riddle; a chart with narration is an insight.
- **Always time-comparable.** Every metric can be overlaid year-on-year (self-vs-self), with the comparison animating between states. Growth is only legible against a baseline.
- **Tap-to-story.** Every data point links back to the *memories* behind it — tap the happiest week and you can watch its Replay. Data is never a dead end; it's always a door back to the lived moment.

### 7.3.1 Specific signature visualizations

- **The Mood Aurora (Year):** a horizontal year-long ribbon of flowing color, height/intensity = mood, hue = energy. Annotated peaks and valleys. Stunning, screenshot-worthy, instantly legible.
- **The Travel Globe:** a slowly rotating dark-mode globe, your visited places glowing, routes drawn as luminous arcs, with stats orbiting (*"23 cities · 9 countries · 14,000 miles"*). Tap a glow → memories there.
- **The Body Story (Fitness):** living rings for the period, a strength-over-time arc, PR badges, and a "strongest period" highlight band. Narrated as a journey, not a stat sheet.
- **The Sleep Sky:** a night-band timeline; consistency, debt, and best streaks shown as constellations. *"Your best sleep was the week after the marathon."*
- **The People Constellation (Social):** the most emotionally potent. People as stars, sized/brightened by presence in your life, clustered by era, lines for shared moments. You can literally *see* who your universe revolves around — and watch stars rise and fade across years. (Handled with the emotional-safety system for faded/lost relationships.)

## 7.4 The Report (A Deep-Dive Into One Insight)

Tapping any award/Lab opens a **Report** — designed to read like a beautifully laid-out feature in a magazine *about you*, scrolling vertically:

1. **Cover** — the superlative headline + hero visualization, full screen.
2. **The evidence** — 2–4 supporting visualizations, each annotated, each tappable to memories.
3. **The narrative** — the AI's written interpretation: what happened, why, and what it might mean. Literary, warm, specific.
4. **The comparison** — how this stacks against your other years/periods (self-vs-self).
5. **The moments** — a rail of the key memories behind the data, each playable.
6. **The reflection / forward look** — *"You were happiest when you were creating. Want to make more space for that?"* — gentle, optional, growth-oriented.
7. **Share** — a pre-composed beautiful share card (Part 10).

A Report is itself a kind of Story (Part 5) — the line between "data Report" and "narrative Story" is intentionally soft; both are the Biographer telling you about yourself, just with different emphasis (numbers-forward vs. narrative-forward).

## 7.5 The Achievements Vault (Lives In You, Powered By Insights)

The achievements system (introduced in Part 1.3.3) gets its home here: a **Vault** of collectible milestone cards — embossed, metallic, dated, with real visual weight and satisfying physics when earned. Categories: distance, strength, consistency, travel, social, learning, and rare "life milestones" (a 10-year streak, a 50th country). Some are **secret** until earned (curiosity). Some are **rare** with special materials (scarcity = pride). The Vault is a personal trophy room — pure achievement emotion, permanent, never expiring.

## 7.6 The "Compassionate Analytics" Doctrine

Because this surface touches sensitive self-judgment, it operates under strict tone rules (an extension of the Life Score doctrine):

- **No metric is ever framed as failure.** Declines are contextualized, never scolded. "Your most-rested period" exists; "your laziest month" never does.
- **We surface the good more than the bad** — the ratio of celebratory to cautionary insights is deliberately skewed positive, because the product's job is to help you love your life, not audit it.
- **Hard truths are offered, not imposed.** If the data shows a worrying pattern (declining sleep, shrinking social world), we surface it *gently and privately, with care and a path forward*, never as a red alert. The Companion delivers these, in conversation, with consent.
- **The user owns the interpretation.** Every AI interpretation is offered as a perspective ("It looks like…"), correctable by the user, never as verdict.

## 7.7 Insights — States & Edge Cases

- **Insufficient data for a superlative:** we don't crown a "happiest year" from two months of data. Locked award cards show *"Unlocks once I've known you a full year"* — aspirational, not empty.
- **Single-year users:** superlatives reframe to within-year ("your happiest *month*") until multi-year comparisons become possible.
- **Sparse dimensions (no fitness data):** that Lab is hidden, not shown broken. We never display an empty chart. We may gently invite connecting a source if it would unlock value.
- **Painful superlatives (e.g., "least social year" during a depression):** suppressed by the compassionate-analytics doctrine; never auto-surfaced.
- **Loading:** visualizations build in with a graceful animated draw (the aurora flows in, the globe spins up, rings fill) — the *construction* of the chart is itself a small delight, masking compute.

---

# PART 8 — AI COMPANION

The Companion is the product's intelligence made conversational — a personal AI that has read your entire life and can talk with you about it. It answers questions like *"What changed in my life since 2023?", "When was I happiest?", "What habits made me successful?", "What months should I revisit?"* This part designs who it is, how it works, and how it looks.

## 8.1 Who The Companion Is (Personality Design)

Before designing the interface, we design the *being.* The Companion's personality is the product's personality, and it must be unmistakable and consistent everywhere (Home's editorial voice, Story narration, Insight callouts, and conversation are all *the same voice*).

**The Companion is:**
- **A warm, perceptive biographer-friend** — not an assistant ("how can I help?"), not a therapist (no clinical framing), not a hype-bot (no fake enthusiasm). Think the most emotionally intelligent friend you have, who happens to remember everything.
- **Reverent about your life** — it finds your life genuinely interesting and beautiful, and it shows.
- **Specific, never generic** — it speaks in *your* particulars ("that week in Lisbon," "the run where you finally broke 25 minutes"), because it actually knows them. Generic AI chatter is the enemy.
- **Honest but kind** — it will tell you a hard truth if you ask, but always with care and a path forward. It never flatters and never scolds.
- **Quietly literary** — a touch of poetry, never purple. It can turn a phrase, but it earns it.
- **Humble about certainty** — "It looks like…", "I might be wrong, but…". It treats you as the authority on your own life.

**The Companion is NOT** a general chatbot. It will gently redirect off-topic requests ("I'm here for your life — ask me anything about *you*"). Its scope is *you*, and that focus is its magic.

### 8.1.1 Naming & identity

The Companion has a name the user can keep as default or personalize. The default is something warm and non-gimmicky (not "Robo," not a human name that implies a fake person). A working default: **"Echo"** — it reflects your life back to you. The user can rename it. It has no fake backstory, no pretend feelings ("I'm so excited!!"), no uncanny human cosplay — it is honest about being an intelligence that knows your life. Honesty is part of the trust contract.

## 8.2 How The Companion Looks (The Orb)

The Companion's visual identity is **The Orb** — a small, living sphere of soft light (see Part 9 for material spec). It is:

- **Omnipresent but unobtrusive** — floating bottom-right on Home/Timeline/Stories; summonable anywhere via swipe-up from the tab bar.
- **Alive** — it breathes (gentle scale pulse), drifts subtly, and its internal light shifts with state: calm when idle, swirling when thinking, warm-bright when it has something delightful to say.
- **Emotionally expressive without a face** — we deliberately avoid eyes/face (uncanny, gimmicky). The Orb conveys "mood" through color, motion, and luminosity. It's closer to a will-o'-the-wisp or a soul than a cartoon assistant.
- **Color-coded to its current intent** — gold when it's surfacing something joyful, cool blue when reflective, soft violet when it's offering a gentle/sensitive observation.

## 8.3 How A Conversation Works (The Interface)

Tapping/summoning the Orb expands it into the **Conversation** — but this is *not* a wall of chat bubbles. We reject the plain-text-messenger paradigm because this product is visual and emotional. Instead:

**The Conversation is a rich, generative canvas.** When you ask *"When was I happiest?"*, the Companion doesn't just type a paragraph — it **composes a response with media**: a sentence of interpretation, *plus* the mood-aurora of that period, *plus* a playable Replay of the happiest week, *plus* a tappable rail of the key memories. Answers are **mini-Reports** (Part 7), assembled live. The Companion *shows*, it doesn't just tell.

**Layout:**
- Conversation rises from the bottom as a glass sheet over a dimmed version of wherever you were (context preserved — you can ask about what you're looking at).
- Your messages are minimal, right-aligned, quiet.
- The Companion's responses are rich cards/blocks that can contain text, visualizations, memory rails, playable Replays, and action chips ("Make this a Story," "Show me more," "Watch it").
- A persistent input at the bottom: text, **voice** (hold-to-talk, big and natural — talking to your life feels right), and suggested-question chips that are *personalized and time-aware* ("Want to see what last weekend looked like?").

**Voice mode (premium-leaning, see Part 11):** a full hands-free, spoken conversation where the Companion talks back in its voice while showing media on screen — like having a documentary narrator who responds to you. This is the most futuristic, magical interaction in the app and a strong premium driver.

## 8.4 What You Can Ask (Capability Design)

The Companion's capabilities map to four modes, all in one conversation:

1. **Retrieval / navigation** — *"Show me the Japan trip," "Find photos with Mom from when I was a kid," "What did I do last New Year's Eve?"* → flies you there / shows the memories. (This is also how Search works — see Part 2/4.)
2. **Analysis / insight** — *"When was I happiest?", "What changed since 2023?", "Am I sleeping worse than last year?", "What habits showed up in my best months?"* → composes a mini-Report with evidence and interpretation.
3. **Creation** — *"Make me a Replay of all my beach days," "Tell the story of my friendship with Sam," "Build a 2026 recap."* → triggers the Replay/Biographer engines and delivers the artifact in-conversation.
4. **Reflection / coaching (gentle, opt-in)** — *"Why do I feel off lately?", "What should I revisit?", "Help me see this year clearly."* → a careful, supportive, evidence-grounded reflection, always with the user as authority, always with the emotional-safety system active. **Never clinical, never prescriptive about health/mental-health** — it reflects and asks, it does not diagnose or treat (a hard ethical/legal guardrail).

### 8.4.1 The proactive Companion

The Companion isn't only reactive. With permission, it **proactively reaches out** with genuinely valuable observations — *"I noticed you've slept better every week you've journaled. Thought you'd want to know."* These arrive sparingly (rate-limited, quality-gated) as Home cards or gentle notifications. Proactivity is the difference between a tool you use and a presence in your life — but over-used it becomes spam, so it's tuned conservatively and fully controllable.

## 8.5 The Trust & Safety Architecture (Non-Negotiable)

Because the Companion knows everything, its trust design is the most important in the product:

- **Local-first / private by design** — the felt guarantee (and, per architecture, the technical one wherever possible) that this is *your* intelligence about *your* life, not a data harvest. Privacy is stated plainly in the Companion's own voice on first meeting.
- **No fabrication** — the Companion answers only from real data; when it doesn't know, it says so. It never invents a memory. A hallucinated memory in *this* product is catastrophic, so the engine is grounded and citations-to-memory are always available ("here's what I'm basing this on").
- **Emotional safety** — the gentle gate (Part 1.5) governs everything; the Companion will not ambush you with grief, will respect muted people instantly, and will tread carefully around hard topics, always offering an exit.
- **Honesty about being AI** — no pretending to be human, no manufactured emotions, no manipulative engagement tactics. The relationship is honest, which is what makes it trustworthy enough to be intimate.
- **Hard guardrails** — no medical/mental-health diagnosis or treatment; crisis-sensitive language detection routes to real human resources with care; never optimizes for engagement at the user's emotional expense.

## 8.6 Companion — Motion, Voice & Feel

- **The Orb's "thinking"** — instead of a spinner, the Orb swirls inward and its light churns; "speaking" radiates gentle pulses. State is always legible through the Orb itself.
- **Streaming, composed answers** — text streams in the warm voice; media blocks resolve in with graceful builds (the aurora flows, the rail slides in). The answer *assembles* like a small production.
- **Voice** — the spoken voice matches the personality: warm, measured, unhurried, never peppy-assistant. Multiple voice options; the default is calm and grounding.
- **Haptics** — a soft pulse when the Companion has finished composing; a warmer one when it surfaces something joyful.
- **Continuity** — the Companion remembers the conversation and your life-context across sessions; reopening feels like resuming with someone who knows you, not starting over with a stranger.

## 8.7 Companion — States & Edge Cases

- **New user / thin data:** the Companion is honest — *"I'm still getting to know you. Ask me what I've found so far, and I'll get sharper every week."* It demonstrates value on whatever data exists rather than overpromising.
- **Question it can't answer from data:** it says so plainly and offers the closest real thing, never fabricates.
- **Off-topic / general-chatbot requests:** gentle redirect to its purpose; it won't become a generic assistant.
- **Sensitive / crisis content:** safety routing as above, with human warmth and real resources, never a canned brush-off.
- **Offline:** retrieval/navigation works on cached data; heavy generation queues with a calm status; the Orb shows a subtle "resting" state.
- **Latency:** the Orb's thinking animation makes waiting feel like *consideration*, not lag; partial answers stream so the user is never staring at nothing.

---

# PART 9 — VISUAL DESIGN SYSTEM

This part defines the complete design language — the system that must feel more premium than Instagram and Apple Photos. It is specified with real values so it is implementable. We call the design system **"Aurora."**

## 9.1 Design Principles (The Aesthetic Constitution)

1. **Cinematic, not appy.** Depth, light, and motion everywhere. The app should feel like a film about your life, not a utility. Reference: Apple TV+ title sequences, not iOS Settings.
2. **Content is the interface.** The user's own photos/memories *are* the backgrounds, the textures, the color. The chrome recedes so the life shines. Our UI is a frame around a masterpiece — the masterpiece is the user.
3. **Dark by default, warm by nature.** A deep, near-black canvas makes photos glow and feels premium and intimate (like a cinema). But never cold — we lean warm, with golden light, never clinical blue-grey.
4. **Glass and light, not flat panels.** Surfaces are translucent, layered, and catch light. Depth communicates hierarchy and makes the app feel like a physical, precious object.
5. **Motion is meaning.** Nothing appears or moves without purpose. Every transition preserves spatial continuity. Motion signals reverence (slow, weighted) or delight (springy, light) deliberately.
6. **Restraint is luxury.** Generous space, few elements per screen, one clear focal point. Cheap apps are cluttered; luxury is what you leave out. (Reference: the empty space in an Apple Store.)
7. **Typography as voice.** Type isn't just legible — it carries the product's literary, warm personality. We use type emotionally, not just functionally.
8. **Earned delight.** Micro-interactions and flourishes reward real moments; we never sprinkle confetti on nothing. Delight is currency; we don't debase it.

## 9.2 Color System

### 9.2.1 The canvas (dark mode is the primary mode)

| Token | Hex | Use |
|---|---|---|
| `canvas/void` | `#000000` | True black — Replay player / cinema only |
| `canvas/base` | `#08080C` | App background (near-black, faint blue-warmth) |
| `canvas/raised` | `#121218` | Raised surfaces base tint |
| `canvas/sunken` | `#050507` | Recessed wells |

The base is *not* pure black for general UI (pure black is harsh and shows OLED smear on scroll); it's a near-black with a whisper of warmth so it reads intimate, not cold.

### 9.2.2 The warm spectrum (our signature — "the golden hour")

The brand's emotional core is **golden-hour light** — the warm, nostalgic glow of memory.

| Token | Hex | Use |
|---|---|---|
| `gold/core` | `#FFB871` | Primary warm accent, "memory" glow |
| `gold/bright` | `#FFD9A8` | Highlights, light blooms |
| `amber/deep` | `#E8853A` | Pressed/active warm states |
| `ember` | `#FF6B4A` | Streak flames, energy |

### 9.2.3 The cool spectrum (reflection, calm, "now")

| Token | Hex | Use |
|---|---|---|
| `aurora/blue` | `#6FA8FF` | Reflective states, "present" content |
| `aurora/violet` | `#A78BFA` | The Companion's sensitive/thinking state |
| `aurora/teal` | `#5EE0C0` | Balance, calm Life Score |

### 9.2.4 The Aurora gradient (the brand signature)

The defining brand object is the **Aurora gradient** — a flowing, multi-stop gradient that blends gold → violet → teal → blue, used in the logo, the Life Score orb, the Companion orb, loading states, and Year/Life Replay title sequences. It is *animated* (slow flow), never static. It is to us what the Instagram gradient or Spotify green is to them — instantly recognizable, ownable, emotional. The Aurora *responds* to context: warmer when content is joyful/nostalgic, cooler when reflective.

### 9.2.5 Semantic & text colors

| Token | Hex | Use |
|---|---|---|
| `text/primary` | `#F5F3EF` | Primary text (warm off-white, never pure white) |
| `text/secondary` | `#A8A29A` | Secondary text |
| `text/tertiary` | `#6B6760` | Captions, stamps |
| `stroke/hairline` | `rgba(255,255,255,0.08)` | Glass borders, dividers |

Note we never use pure `#FFFFFF` text — warm off-white (`#F5F3EF`) reduces harshness and reinforces the golden, filmic warmth.

### 9.2.6 Light mode

Light mode exists (accessibility, daytime preference) but is the *secondary* mode and explicitly designed to be just as premium: a warm paper-white canvas (`#F7F4EE`, not clinical white), the same gold/aurora accents, soft shadows replacing glass-glow, and photos framed in warm neutrals. It reads like "fine gallery print" vs. dark mode's "cinema." The brand and emotion survive the mode switch intact.

## 9.3 Typography

Type carries the voice. We use a **two-typeface system** with a deliberate emotional split:

- **Display / Memory serif — a humanist serif** (e.g., *Canela*, *Tiempos*, or *Newsreader* as a base). Used for: memory captions, Story narration, Replay title cards, Insight superlatives, the Companion's most heartfelt lines. The serif signals *humanity, literature, timelessness.* It is the voice of memory.
- **Interface sans — a clean geometric-humanist sans** (e.g., *SF Pro / Inter / a custom grotesque*). Used for: UI labels, navigation, data, controls. Quiet, legible, gets out of the way.

This split is core: **serif = emotion/memory, sans = function.** When the app wants you to *feel*, it speaks in serif; when it wants you to *do*, it speaks in sans. Users feel this difference even if they never consciously name it.

### 9.3.1 Type scale (sans UI scale, pt)

| Token | Size / Line | Weight | Use |
|---|---|---|---|
| `display-xl` | 44 / 48 | Serif Light | Replay/Insight hero superlatives |
| `display-l` | 32 / 38 | Serif Regular | Story titles, section heroes |
| `title-1` | 24 / 30 | Sans Semibold | Screen titles |
| `title-2` | 20 / 26 | Sans Semibold | Card titles |
| `body-l` | 17 / 25 | Sans Regular | Primary body |
| `body` | 15 / 22 | Sans Regular | Standard text |
| `caption` | 13 / 18 | Sans Medium | Stamps, metadata |
| `micro` | 11 / 14 | Sans Medium | Labels, tags |
| `memory` | 22 / 32 | Serif Italic | Memory captions / narration (signature) |

Numerals are tabular in data contexts (charts align), proportional in prose.

## 9.4 Spacing & Layout

An **8pt soft grid** with a generous baseline. Luxury = space.

| Token | Value |
|---|---|
| `space/1` | 4 |
| `space/2` | 8 |
| `space/3` | 12 |
| `space/4` | 16 (base gutter) |
| `space/5` | 24 |
| `space/6` | 32 |
| `space/7` | 48 |
| `space/8` | 64 |
| `space/9` | 96 (section breaks, "breath") |

- **Screen margins:** 20pt default; 16pt on dense surfaces.
- **Card corner radius:** 28pt for hero cards, 20pt standard, 16pt small chips, 999pt for pills/orb. Generous, soft, Apple-grade roundness — never sharp corners (sharp = clinical/cheap in our language).
- **One focal point per viewport.** Every screen has a single clear hero; everything else is demonstrably subordinate in size/contrast/position.

## 9.5 Glassmorphism (The Material System)

Glass is our signature material. But cheap glass (uniform blur) looks dated; ours is **layered, light-responsive glass** with a precise spec:

- **Backdrop blur:** 24–40px gaussian, plus a subtle saturation boost (+15%) so colors behind glow through richly.
- **Fill:** `rgba(20,20,28, 0.55)` over dark content (adapts to content luminosity — it lightens over bright photos so text stays legible; this adaptive tint is what separates premium glass from a flat overlay).
- **Border:** a 1px `stroke/hairline` top-light edge — a brighter hairline on the top/left, fading to nothing on bottom/right, simulating a light source above. This single detail makes glass read as a *physical pane* rather than a flat rectangle.
- **Inner glow / specular:** a faint radial highlight where light "hits" the glass, animating subtly as the device tilts (gyroscope-driven specular — a luxury touch borrowed from physical product design).
- **Depth shadow:** soft, large, low-opacity (`0 20px 60px rgba(0,0,0,0.45)`) to float glass above content.

Glass is used for: tab bar, the Companion conversation sheet, Director panel, modal sheets, contextual controls. **Glass is for chrome; content is never behind glass.** The user's memories are always crisp and front; only our UI is glass.

## 9.6 Cards (The Core Component)

Cards are the atomic unit of Home, Stories, Insights, Replay rows. Spec:

- **The Memory Card** — full-bleed media, 28/20pt radius, content (caption/stamp) in a bottom gradient scrim (`transparent → rgba(0,0,0,0.7)`) so text is always legible over any photo. Media *breathes* (subtle scale loop) on hero cards. On press: scales to 0.97 with a soft spring + light haptic. On expand: shared-element zoom to full screen.
- **The Data Card** (Insights) — glass-framed, a visualization + an AI callout + a superlative. Animates its visualization in on appear.
- **The Achievement Card** — opaque, materially rich (metallic/embossed), with weight and specular; seats with a "thunk" haptic when earned.
- **Elevation language:** three levels — flat (content), raised (glass chrome), floating (orb, FAB, active card). Elevation shown via shadow softness + specular intensity, not hard borders.

## 9.7 Motion System

Motion is how we signal reverence and delight. The system has **two named motion personalities**, used deliberately:

- **"Reverent" motion** — slow, weighted, eased. Spring with high damping; durations 500–900ms. Used for: memory reveals, Replay opens, Story transitions, anything emotional. It says *this matters, slow down.*
- **"Lively" motion** — quick, springy, slightly overshooting. Lower damping; 250–400ms. Used for: UI controls, taps, toggles, navigation. It says *this is responsive and alive.*

### 9.7.1 Motion tokens

| Token | Curve | Duration |
|---|---|---|
| `motion/reverent` | spring(stiffness 120, damping 26) | 600–900ms |
| `motion/lively` | spring(stiffness 320, damping 24) | 250–400ms |
| `motion/instant` | ease-out | 120ms (taps, highlights) |
| `motion/cinematic` | custom bezier (0.16, 1, 0.3, 1) | 800ms+ (Replay/Story opens) |

### 9.7.2 Signature transitions

- **Shared-element zoom** — every card→detail is a continuous zoom of the *same* element; we never hard-cut between screens. The user's spatial model is never broken.
- **The theater dim** — Replay opens dim the world before the film (Part 6).
- **Pull-to-Remember time-warp** — the screen color-grades older as you pull (Part 1.4).
- **Pinch-through-time** — continuous temporal zoom (Part 4).
- **The gather** — memories swirling into form (onboarding, generation waits).
- **Aurora flow** — the brand gradient perpetually, slowly flowing in hero/loading/orb contexts.

### 9.7.3 Reduced motion

A full reduced-motion mode (respecting OS setting) replaces parallax, breathing, and Ken Burns with gentle cross-dissolves and static compositions — while *preserving narrative and emotion.* Accessibility never means a lesser emotional experience, just a calmer one.

## 9.8 Micro-Interactions (The Soul Is In The Details)

These tiny moments are where "premium" is actually felt:

- **Press feedback** — every tappable element scales 0.97 + soft haptic; release springs back. Universal, consistent, satisfying.
- **The Hold-to-Replay bloom** — pressing a memory blooms a soft ring of light outward as it begins to play under your finger.
- **Streak ember flicker** — streak icons literally flicker like flame, brighter with longer streaks.
- **Milestone seat** — achievement cards drop and *seat* with a weighted thunk + haptic, like setting a medal on a table.
- **Pull-to-Remember resistance** — the pull has physical rubber-band resistance; the date readout scrubs with tiny ticks; a soft chime as you "land" on an era.
- **Orb breathing** — the Companion always gently breathes; you feel it's alive even when idle.
- **Number roll-ups** — stats count up with eased deceleration (never just appear) — the accumulation of your life feels *earned* as it tallies.
- **Gyroscope parallax & specular** — hero images and glass shift subtly with device tilt — the app has *depth you can feel* in your hand.
- **Haptic vocabulary** — a deliberate set: light tick (navigation), soft pulse (selection), warm double-pulse (delight/joy surfaced), weighted thunk (achievement), gentle swell (Replay peak). Haptics are *composed*, not random, and fully disable-able.
- **Sound (optional, off in silent contexts)** — a tiny, tasteful sonic palette: a soft "page" for Story advances, a warm chime for milestones, the film-reel whir for scrubbing. Sound is *designed*, sparse, and never annoying.

## 9.9 Iconography & Imagery

- **Icons** — a custom set, rounded, light-weight strokes (1.75pt), slightly soft — matching the warm, humane personality. No sharp/technical icons. Active states glow with the relevant accent rather than just filling.
- **The user's photos are the imagery.** We commission almost no stock art. Where we need illustration (empty states, onboarding), we use soft, abstract, light-and-gradient forms consistent with Aurora — never literal clip-art. Empty states feel like *potential*, rendered as gentle dawn-light gradients, not sad blank boxes.

## 9.10 Why This Exceeds Instagram & Apple Photos

- **Instagram** is a flat, bright, content-dense feed optimized for advertising — it's loud. We are dark, spacious, cinematic, and quiet — optimized for *feeling.* Premium is calm; Instagram is not calm.
- **Apple Photos** is beautiful but *clinical and utilitarian* — it's a library, neutral and grid-bound, with Memories as a feature bolted on. We are emotional and narrative *to the core*, with a literary voice, a living material system, and motion that signals reverence. Apple shows your photos; we tell your story.
- **Our edge** is the *coherence* of an emotional system: the serif-for-memory voice, the golden-hour palette, the Aurora signature, the two motion personalities, the adaptive glass, and the rule that content always outshines chrome. No competitor has a design language this emotionally specific and this disciplined at once.

---

# PART 10 — VIRALITY

The product's growth engine. How do we make users share, create a Spotify-Wrapped moment, build social loops, and drive emotional sharing — *without* becoming a social network (our anti-goal, Part Preamble)? This part designs growth that stays true to the product's soul.

## 10.1 The Core Tension (And Its Resolution)

We refuse a social feed, follower counts, and stranger-validation — those are the things that make modern apps anxiety machines. But we still need viral growth. The resolution: **we make the artifact shareable, not the user social.** Users share *outward* (to their existing networks — Instagram, iMessage, TikTok), not *inward* (to a feed inside our app). We are a content *factory* for the rest of the internet, and every shared artifact is an ad for the product that the recipient *wants* to watch.

This is the BeReal / Spotify Wrapped model, not the Instagram model: virality through *exported artifacts* that carry the brand, not through an in-app social graph.

## 10.2 The Spotify-Wrapped Moment: "Life Replay: The Year"

Our supernova growth event is the **annual Year Replay drop** (Part 6.4.4), engineered explicitly as a cultural moment bigger than Wrapped — because ours is *cinematic and about your whole life,* not just your music.

**The mechanics of the moment:**
- **A coordinated global drop.** Each December, "Your 2026 Replay is ready" lands for everyone in a ~2-week window, manufacturing collective cultural energy (the thing that makes Wrapped trend). Everyone's doing it at once → social proof → FOMO → installs.
- **The artifact is a film, not a stat card.** Where Wrapped shares static slides, we share a *cinematic 60-second vertical film of your year* — scored, narrated, color-graded, gorgeous. Infinitely more shareable on TikTok/Reels/Stories because it's *motion content* the platforms favor.
- **Shareable "stat moments" too.** Within the year film, we generate individual shareable cards for the punchy stats ("14,000 miles," "Word of the year: *again*," "40 new faces") — the screenshot-bait Wrapped perfected — but rendered in our cinematic Aurora language.
- **The pre-drop tease.** A countdown on Home ("Your year is almost ready") builds anticipation for weeks. Anticipation is half the virality.

**Why it beats Wrapped:** Wrapped is about your *consumption* (what you listened to). Ours is about your *life* (who you became). The emotional payload — and therefore the share impulse — is an order of magnitude higher. People share Wrapped to signal taste; they'll share Life Replay to share *meaning.*

## 10.3 Beyond Once-A-Year: The Always-On Share Engine

A once-a-year event isn't a growth engine alone. Every emotional surface has a **frictionless, beautiful share path**:

- **Any Replay** (day/week/month/themed) → "Share this" → renders a vertical, watermarked, music-scored clip optimized for the destination platform.
- **Any Story** → share the cinematic trailer of that Story.
- **Any Insight superlative** → a gorgeous stat card ("My happiest year was 2024").
- **"This Day, Every Year"** (Part 3.3.2) → the aging-through-one-date montage — uniquely mesmerizing, highly shareable.
- **Milestones** → "I just ran my 500th mile with Life Replay" auto-composes a celebration card.

### 10.3.1 The Share Composer (unified, premium)

We never dump to the OS share sheet raw. The **Share Composer** (Part 2.4) gives a moment of pride and control:
- Live preview of the beautiful artifact.
- Format auto-optimized per destination (9:16 for Stories/TikTok, 1:1 for feed, link for messages).
- **Privacy gate front-and-center** — choose what's included; faces of others can be blurred/excluded with one tap (consent-respecting by design — never share someone else's face without ease of removing it); a clear "this is what others will see" preview.
- Tasteful, *removable* watermark (a small Aurora mark + "Made with Life Replay") — present by default (growth), removable for premium (Part 11). The watermark must be beautiful enough that people *don't mind* it — it's a design flex, not a logo slap.

## 10.4 The Social Loops (Honest Ones)

We engineer loops that grow the product without a social feed:

1. **The artifact loop** — User makes a Replay → shares to TikTok → 10,000 strangers see a stunning film + watermark → "what app is this?" → installs. The shared content *is* the acquisition channel. Highly cinematic content travels far on algorithmic platforms.
2. **The "make mine" loop** — Seeing a friend's Life Replay triggers "I want to see *mine*" far more powerfully than seeing their feed post. Self-directed curiosity > social comparison. This is the Wrapped mechanism, and it's the healthiest viral loop in tech.
3. **The shared-memory loop (opt-in, careful)** — For memories *with* other people, a "send this to [person you were with]" path: "You were both there — share this moment with Sam." This spreads the product through *genuine shared experiences*, not broadcast. The recipient gets a gift (a memory of *them*), and a soft install prompt. Real, warm, non-spammy.
4. **The collaborative Replay (premium social, opt-in)** — two people who share an experience (a trip, a relationship) can *merge* their memories into one co-created Replay. This is the only "social" feature, and it's intimate (1:1 / small group), not a feed. It's also a powerful invite vector ("Sarah wants to make a Trip Replay with you — join").

## 10.5 Emotional Sharing (Why People Will Actually Share)

People share what makes them *feel* and what makes them *look good/meaningful.* Our shares hit both:

- **Identity signaling, elevated** — sharing your "Most Growth Year" or "My Fitness Journey" Story signals who you are and who you're becoming. It's aspirational self-presentation that's *true* (grounded in real data), which feels better to share than a posed photo.
- **Genuine emotion** — a Life Replay or a "This Day, Every Year" montage makes the *sharer* cry; content that moves the creator gets shared, because they want others to feel it too.
- **The gift frame** — sharing a shared-memory to the person in it is an *act of love*, not self-promotion. These shares have the highest conversion because they arrive as gifts from someone you trust.

## 10.6 Acquisition & Onboarding-For-Virality

- **The shared artifact is the landing page.** A non-user who taps a shared Replay lands on a web player that plays the full beautiful film, *then* says "This is [friend]'s. Yours is waiting" → App Store. The wow happens *before* install (reverse of the usual funnel).
- **Genesis Replay as referral payoff** — referred users get their Genesis Replay (Part 1.2) instantly; the wow that converted the sharer now converts the recipient. The product *is* its own best ad.
- **Restraint as a growth feature** — because we *don't* spam, don't sell data, and don't manufacture anxiety, the product earns word-of-mouth trust that paid acquisition can't buy. "It's the one app that's actually good for you" is a viral message in itself.

## 10.7 Virality — Guardrails (Staying True To The Soul)

Growth must never corrupt the product's emotional integrity:
- **No public profiles, no followers, no likes-from-strangers, ever.** (Anti-goal.)
- **No dark patterns** — no "share to unlock," no guilt, no fake scarcity beyond the genuine annual moment.
- **Privacy-first sharing** — others' faces/data never leave without explicit, easy consent control.
- **Never auto-share, never share without preview.** The user always sees exactly what goes out.
- **Sensitive content is never made shareable by default** — grief/hard content has the gentle gate even in sharing.

The thesis: **the most viral thing we can build is a product so emotionally good that people can't help but show it to the people they love.** Growth is a byproduct of meaning, not a feature bolted onto it.

---

# PART 11 — PREMIUM FEATURES

What would people happily pay for, every month, for a product about their own life? This part designs the monetization — the tiers, the value, and the *principle* that keeps monetization from poisoning the emotion.

## 11.1 The Monetization Principle: "Never Paywall The Soul"

The free experience must be *genuinely, completely emotionally satisfying.* We never paywall feeling. A user who never pays must still fall in love with the product — because (a) it's the right thing for a product about someone's life, and (b) free users are the viral engine (Part 10), and (c) emotional attachment is what *eventually* converts.

So we follow one rule: **free gives you the emotion; premium gives you more of it, deeper, and to keep.** We paywall *depth, fidelity, scope, and ownership* — never the core feeling.

What this means concretely:
- **Free users get:** the Genesis Replay, daily Home, the Timeline, weekly/monthly Replays, basic Stories, core Insights, the Companion (rate-limited), and the annual Year Replay (the viral moment — *never* paywalled, that would kill growth). The free product is a complete, beautiful, daily-lovable app.
- **Premium users get:** the things that turn a beloved app into an indispensable life-archive.

## 11.2 The Tiers

We use a clean **three-tier** structure (free + two paid), avoiding tier-sprawl.

### Tier 1 — Free ("Life Replay")
The complete emotional core, as above. Generous on purpose. The job of free is to make you love the product and tell your friends.

### Tier 2 — Premium ("Life Replay+") — the main subscription
**Target price: ~$9.99/month or $79.99/year** (annual heavily favored; the value is long-term, so is the pricing). Positioned as "the price of a couple coffees to own the movie of your life." For what people get, this is a steal — and the annual framing (under $7/mo) lands easily for an emotional product.

**What Premium unlocks:**
- **The full Life Replay** — the crown jewel (Part 6.4.5) in full fidelity, the whole-life film. The single strongest paywall: people will pay specifically to watch the complete movie of their life.
- **Unlimited & on-demand Replays and Stories** — generate any themed Replay, any custom Story, any time, instantly ("make me a Replay of every birthday"). Free is rate-limited; Premium is unlimited creativity.
- **Higher fidelity & cinematic engine** — 4K/HD exports, premium scores/soundtrack library, AI voice narration, advanced color grading, the Director controls (Part 6.6).
- **Unlimited Companion + Voice mode** — the full conversational, hands-free, talk-to-your-life experience (Part 8.3). Free gets a daily allowance; Premium gets unlimited + voice.
- **Deep Insights & all Labs** — the full analytics suite, all dimensions, all comparisons, downloadable life-reports.
- **Watermark-free, high-res sharing** — clean exports for the proud sharer (the watermark stays free → viral; removing it is a premium perk).
- **Full history depth** — free might surface the last N years in rich detail; Premium gives unlimited historical depth and resolution.
- **Priority generation** — Premium Replays/Stories render first.

### Tier 3 — "Legacy" (the premium-premium / family tier)
**Target price: ~$24.99/month or $199/year** (or a higher one-time "forever" option — see 11.4). For the deeply committed, families, and the legacy-minded.

**What Legacy adds on top of Premium:**
- **Family / shared archives** — collaborative Replays and shared family timelines (Part 10.4); a *family* Life Replay merging multiple members' memories (an extraordinarily emotional artifact — a family's whole history as one film).
- **Multi-person Stories** — "Our family's decade," "Mom & Dad's story."
- **The Legacy Vault** — guaranteed long-term, redundant, exportable preservation of the full archive (the "this outlives me" promise — see 11.3).
- **Inheritance / time-capsule features** — designate someone to receive your Life Replay; create "open in 10 years" capsules.
- **The highest-fidelity, longest Life Replays** and earliest access to new capabilities.

## 11.3 Why People Will Happily Pay (The Value Thesis)

People pay monthly for things that are **emotionally indispensable** and **identity-tied.** Life Replay+ is both:

1. **It's the movie of your life — and the most precious one only Premium completes.** Once someone has *felt* the Genesis Replay and a Year Replay, the full Life Replay is irresistible. We're not selling features; we're selling the complete version of the most emotional artifact they own.
2. **Loss aversion is real and ethical here.** As the archive deepens over months, the thought of losing it (or never seeing it whole) is powerful. We don't manufacture fake scarcity — the value is genuinely cumulative, so the longer you use it free, the more obvious Premium becomes.
3. **It compounds.** Unlike a streaming subscription (content you don't own), this is *your* life getting richer and more navigable every month. The value curve only goes up.
4. **It's a tiny price for a huge emotional return.** "$7/month to watch and keep the movie of my life" is one of the easiest value propositions in consumer software.

## 11.4 Monetization Mechanics & Design

- **The conversion moment is emotional, not transactional.** We never interrupt a tender moment with a paywall. The upsell appears at *peaks of demonstrated value* — e.g., right after the user watches a free Replay and clearly wants more, or at the locked Life Replay tile: *"You've lived a remarkable life. Watch the whole film."* Value precedes the ask (Law 3), always.
- **The paywall is beautiful and honest.** No dark patterns, no fake countdowns. A gorgeous screen that shows *exactly* what Premium adds, with a generous free trial (the trial generates a real premium artifact — e.g., a sample full Life Replay — so the user *feels* the value before paying).
- **Annual-first pricing.** The value is long-term; we nudge annual with clear savings, because retention on an emotional life-archive is naturally high (low churn = we can price fairly).
- **A "forever" option (Legacy).** A higher one-time lifetime purchase appeals to the legacy-minded who hate subscriptions and want permanence — and it aligns with the "this outlives me" promise.
- **No ads, ever.** Ads would shatter the reverence and the trust. Our anti-surveillance positioning is a *feature* and a moat; we monetize the user, honestly, not their data.

## 11.5 Premium — Guardrails

- **Never paywall emotional safety, privacy controls, data export, or deletion.** These are rights, not features.
- **Never paywall the annual Year Replay** — it's the growth engine.
- **Never degrade the free experience to coerce upgrades.** Free stays genuinely great; Premium is *additive*, never created by crippling free.
- **Free trial must deliver a real premium artifact**, so the decision is informed, not tricked.
- **Cancel must be one tap, honored immediately, with the archive preserved** (you keep what's yours). Respectful offboarding builds the trust that drives re-subscription and referral.

---

# PART 12 — 10/10 PRODUCT CRITIQUE (THE STEVE JOBS REVIEW)

*The following is written in the voice of a ruthless founder-critic reviewing the design above. It is intentionally harsh, because flattery doesn't ship great products. Every weakness below is followed by a redesign that pushes the product to world-class.*

---

*[Sits down. Doesn't look at the slides. Looks at the prototype.]*

Okay. It's good. Most of it is *good*, and "good" is exactly the problem, because good is the enemy of insanely great. Let me tell you everything that's wrong with this, and then let me tell you how we fix it. I'm not going to be nice about it.

## Critique 1 — "The whole thing is passive. You built a TV." ❌

**The problem:** Read it back. Watch. Read. Watch. Scroll. The user is a *couch*. You've built the world's most beautiful television for a channel about themselves. But the deepest human emotion isn't *watching* your life — it's *feeling seen* and *being moved to act.* A TV doesn't change anyone. You're one tap away from being a very pretty screensaver people stop opening in March.

**Why it's fatal:** passive products have a ceiling. Beautiful passive products have a *higher* ceiling, but they still plateau, because once I've seen my Genesis Replay and a couple Year Replays, the novelty curve bends down. You're betting the entire retention model on "the editor finds something new daily," and on a quiet life, some weeks it won't. Then I'm watching reruns of myself.

**The redesign — make the product *participatory and generative of real life.***
1. **The product must change the user's actual life, then show them the change.** Add the **"Living Intentions" loop**: the Companion notices what made you happiest/strongest ("you light up around water," "you sleep best when you train") and helps you *do more of it* — not as a nagging habit-tracker, but as a gentle co-author of your future. Then it *closes the loop*: "Three weeks ago you said you wanted more time outside. You've doubled it. Here's the proof." Now the app isn't a TV — it's a *mirror that helps you become who you want to be, and shows you the evidence.* That's not a screensaver. That's indispensable.
2. **The evening reflection becomes the heartbeat, not a footnote.** I buried it as "optional" in Part 1.6 and Part 3. Wrong. The single daily *active* moment — one tap on how today felt, one optional sentence — is the most valuable data we collect AND the most therapeutic thing we offer. Promote it. Make it a gorgeous 10-second nightly ritual that people *crave* — the bookend to their day. That's the active hook a passive product is missing.

## Critique 2 — "The first 60 seconds are a magic trick. What about day 60?" ❌

**The problem:** The Genesis Replay is *phenomenal* — genuinely the best onboarding I've seen described. But you spent 80% of your emotional ammunition in the first minute. You've designed a firework. Fireworks are for the launch. What's the *campfire* — the thing that keeps people warm every night for years?

**Why it's fatal:** retention isn't won at the peak; it's won in the *boring middle.* Tuesday in February, nothing happened today, the user is tired. Does the app still earn the open? Your Home leans hard on "the editor finds something new," but a finite editor + a quiet life = repetition, and repetition kills.

**The redesign — engineer the "infinite well" and the "slow reveal."**
1. **The Slow Reveal:** the app should *deliberately withhold* and *gradually unlock* depth over months and years, so there's always a next discovery. "You've now used Life Replay for 100 days — I can finally show you something I've been noticing." Long-horizon locked content (the Life Replay is one example, but make it a *system*) gives a quiet life a reason to return for years. Anticipation is the renewable fuel novelty isn't.
2. **The infinite combinatorial well:** themed Replays (Part 6.5) are the answer to "nothing new today" — but I under-sold them. They should be a *first-class daily surface*, not a row. "A film of yourself you've never seen" is generable forever from a finite life because the *angles* are infinite. Make the Companion proactively surface a fresh, surprising themed cut on quiet days. The life is finite; the stories about it are not.

## Critique 3 — "The Life Score is a churn bomb with a bow on it." ⚠️

**The problem:** You *know* this — you wrote three paragraphs defending it. When a designer writes three paragraphs defending one component, that component is wrong. Any single number/weather-report summarizing "how your life is going" will, on a bad day, feel like the app *agreeing* that you're failing. The compassionate framing helps, but you're playing with a live grenade for a feature that — be honest — is *table-stakes mimicry* of fitness apps, not core to your soul.

**The redesign — kill the score as a *destination*; keep the *intelligence* as a *whisper.***
- There is no "Life Score" module sitting on Home staring at me. Instead, the *intelligence* behind it lives entirely inside the Companion and surfaces **only when it has something genuinely helpful and kind to say**, in context, in language — never as a standing scoreboard I check and get judged by. "You've been quiet lately, and last time that happened it was the start of something good" is a *gift from a friend.* A 61/100 orb on my home screen is a *verdict.* Ship the friend. Kill the verdict. (This revises Part 3.3.3.)

## Critique 4 — "Everything is gold-hour warm and slow. It's monotonous. It's *one note*." ⚠️

**The problem:** You're so proud of "cinematic, reverent, golden, slow" that the entire app is one emotional temperature. Reverence *everywhere* is reverence *nowhere* — if every screen is sacred and slow, nothing stands out as sacred. Real films have silence AND noise, stillness AND chaos. Your app only has tasteful piano. Where's the *joy* that's loud? Where's the *energy*? You'll feel premium and slightly *funereal.*

**The redesign — give the product dynamic emotional range.**
- Codify **emotional contrast** as a design principle (revising Part 9). The product needs registers: the *reverent* (memory, loss, growth — slow, warm, serif), but ALSO the *euphoric* (a PR, a trip, pure joy — fast, bright, loud, kinetic, even a little chaotic), and the *playful* (surprise themed Replays, delight moments). A "best day of the year" Replay should feel *euphoric and electric*, not like a meditation app. Map each emotional moment to its register and let the app's tempo and palette *swing.* Range is what makes the high notes land.

## Critique 5 — "You're asking me to give an app my entire life. I don't trust you, and your design didn't earn it." ⚠️

**The problem:** You treated privacy as a *system* (good) but you treated it as *defense* — "look how careful we are." Defense doesn't build trust; it signals there's something to defend. And practically: you front-load the biggest ask in tech history (Photos + Health + Location, all at once, in the first 22 seconds) *before* I've felt almost any value. The Genesis Replay is great, but I have to hand over my soul to *get* it. That's a huge faith-leap and your grant rates will bleed.

**The redesign — make trust a *felt, demonstrated, progressive* experience.**
1. **Earn permissions progressively.** Don't ask for everything up front. Ask for *Photos only* to make the Genesis Replay. *Then*, once I'm in love, reveal: "Want me to add your runs to the story?" → Health. "Want to see where your life happened?" → Location. Each ask is now *motivated by a value I've already felt.* Grant rates soar and trust compounds. (Revises Part 1.2.)
2. **Make privacy *visible as a feeling*, not a policy.** A recurring, beautiful "this stayed on your device / this is only yours" motif — a small lock that *glows warm* rather than cold, present at emotional moments, not buried in settings. Trust you can *see* beats trust you have to *read.*
3. **Prove it once, unforgettably.** Early on, a single magical demonstration: show me something deeply personal the app figured out, alongside "and I worked this out without anyone but you ever seeing it." Demonstrated discretion >>> promised discretion.

## Critique 6 — "The empty state IS the product for the first month, and you hand-waved it." ❌

**The problem:** You said "we hide thin surfaces" and "lean on the Genesis Replay's afterglow." That's not a plan, that's a prayer. The hardest design problem in this entire product is the user with a *thin or new photo library* — the 19-year-old, the person who just got a new phone, the person who isn't a photo-taker. For them, day 2 through day 30 is mostly *emptiness*, and emptiness is where you die. You designed the cathedral and forgot most people walk in with three photos.

**The redesign — design the "cold start" as a *flagship* experience, not an edge case.**
1. **Ingest more than photos at the start.** A life leaves many traces: music history, location history (even without photos, your *movements* tell a story), messages *metadata*, calendar, step counts, app usage. For the photo-poor user, *build the first Replay from movement and music and rhythm* — "here's the shape of your last month: where you went, what you listened to, how you moved." Prove the magic works even with no photos.
2. **The "seed your story" onboarding for thin libraries** — a delightful, *active* first session where the user adds a few defining memories/people/milestones by hand (not a chore — a "tell me the headlines of your life so far" guided moment that itself feels emotional). Now even an empty library has a spine.
3. **Forward-looking value from day 1** — for the thin user, reframe the whole product as "let's start capturing your life *beautifully from today*" — so the value is beginning *now*, not only mining the past. The app is a *camera for your future*, not just an archive of your past. This doubles the addressable market (you no longer require a rich pre-existing library).

## Critique 7 — "Five spans of Replay, all the same idea. Where's the *one* feature people will describe in a sentence to a stranger?" ⚠️

**The problem:** Day/Week/Month/Year/Life is a *menu*, not an *idea.* It's the same concept at five durations. Spotify Wrapped is *one* idea you can say in four words. BeReal is *one* idea. What's the four-word version of Life Replay that a stranger repeats at dinner? "Watch the movie of your life" is close — but the *Life Replay* is gated and rare, so the thing people experience daily isn't the thing that's quotable.

**The redesign — anoint and obsess over ONE signature, daily-magical artifact.**
- The hero isn't "Replays (plural)." It's **"This Day, Every Year"** *and* the **daily themed cut** — the *small, daily, shareable, repeatable* magic — backed by the *Life Replay* as the awe-inspiring crown. One daily-quotable hook + one lifetime-awe peak. Pour disproportionate craft into the *one* artifact people will screenshot and text to a friend on a random Tuesday. A product needs a *verb*, not a feature matrix. (Sharpens Part 6.)

## Critique 8 — "It's gorgeous and it has no edges. Where does it *hurt*?" ⚠️

**The problem:** The whole document is warm, safe, kind, gentle, compassionate. Beautiful. But the most *meaningful* products have a point of view that occasionally makes you uncomfortable in a *good* way. Your "emotional safety" system is so protective it risks making the product *toothless* — a yes-man that only ever shows you the nice parts. A life that's only highlights is a lie, and people can feel a lie. The deepest emotion — catharsis, growth, perspective — comes from *honestly* confronting the hard parts, gently.

**The redesign — courage, held with care.**
- The product should be willing, *with consent and exquisite care*, to show you the hard, true things — because that's where the real meaning is. "The year you struggled" is a more powerful Story than "the year you traveled," *if handled with love.* The emotional-safety system should be a *guide rail for honesty*, not a *muzzle.* The bravest, most-loved version of this product is the one that helps you make peace with your whole life, not just enjoy the pretty bits. That courage — disciplined by care — is what separates a *profound* product from a *pleasant* one. (Deepens Part 1.5 / Part 5.)

## Critique 9 — Smaller cuts (the thousand details)

- **The Orb is named "Echo."** An echo is a *fading repetition* — subtly sad, and it implies the app just parrots you back. Wrong metaphor for a forward-looking companion. *Rename.* Something that implies seeing-and-becoming, not repeating. (Minor, but names matter — they're the most-used word in the product.)
- **Tabs vs. soul:** you have a center "Replay" button (good) but the *Companion* — arguably the most magical thing — is a floating orb that's easy to ignore. Decide: is the magic the Replay or the Companion? You can't have two heroes. *Pick.* (My instinct: the Companion is the long-term moat; the Replay is the hook. Lead acquisition with Replay, lead retention with the Companion — and design the hand-off between them explicitly.)
- **"Finite Home that ends" is brave and right — but you didn't say what happens at the end for a power user who wants more.** Don't dump them into a void or a feed. The end should hand them to *one* deliberate next action (their choice, set once): reflect, explore the Timeline, or talk to the Companion. Intentional, not infinite.
- **Performance is mentioned but not *sacred*.** 60fps on the Timeline and buttery Replay playback aren't "budgets" — they're *the entire premium thesis.* One stutter and the magic dies. This deserves to be Law 6, not a footnote.

## Critique 10 — The verdict

*[Stands up.]*

Here's the truth: the *bones* are world-class. The Genesis Replay, the river Timeline, the Biographer, the serif-for-memory typography, the "comparison-with-self-not-others" thesis — that's a 9. That's genuinely special. I'd fund it.

But it's a 9 that *thinks it's a 10*, and that's dangerous. The gap between this and insanely great is four things, and they're all the same thing wearing different clothes:

1. **Stop being passive. Help people *become*, then show them.** (Critique 1)
2. **Solve the boring middle and the cold start, not just the magic minute.** (Critiques 2, 6)
3. **Have emotional *range* and the *courage* to be honest.** (Critiques 4, 8)
4. **Find the one quotable verb and obsess over it.** (Critique 7)

Do that, and you don't have a beautiful app about the past. You have a product that makes people feel *seen, known, and capable of becoming more* — every single day. That's not a memory app. **That's a relationship with your own life.** And people don't churn out of a relationship with their own life.

*That's* the 10. Now go make it.

---

## 12.1 The Redesign, Consolidated (What Actually Changes)

For the team, the critique above resolves into these concrete revisions to the spec:

1. **Add the "Living Intentions" loop** (Companion-driven): notice → gently encourage → prove the change. Promote the **evening reflection** to a first-class daily ritual (the active heartbeat). *(Revises Parts 1, 3, 8.)*
2. **Build the "Slow Reveal" system**: long-horizon, time-gated unlocks so there's always a next discovery for years. *(Revises Parts 3, 6.)*
3. **Elevate themed Replays + "This Day, Every Year" to the daily hero artifact**; the Life Replay is the gated crown. One daily-quotable hook + one lifetime peak. *(Revises Part 6.)*
4. **Kill the Life Score as a standing module**; move its intelligence into the Companion as contextual, kind whispers. *(Revises Part 3.3.3.)*
5. **Codify emotional range** (reverent / euphoric / playful registers) as a design law; let tempo and palette swing. *(Revises Part 9.)*
6. **Make permissions progressive** (Photos → value → Health → Location) and make **privacy a visible, warm, felt motif.** *(Revises Parts 1, 9.)*
7. **Treat cold-start / thin-library as a flagship experience**: ingest movement+music+rhythm, "seed your story" onboarding, and reframe the product as a *beautiful camera for your future*, not only an archive of your past — doubling the market. *(Revises Parts 2, 3.)*
8. **Give the product courage**: the emotional-safety system becomes a guide rail for *honest, caring* confrontation with the whole of a life, not a muzzle. *(Revises Parts 1.5, 5.)*
9. **Rename the Companion** away from "Echo" toward a seeing/becoming metaphor; **explicitly choose Replay-as-hook, Companion-as-moat**, and design the hand-off. *(Revises Part 8.)*
10. **Promote performance to a constitutional Law (Law 6): "Buttery or it didn't ship."** 60fps Timeline, instant Replay playback, no jank — the premium thesis lives or dies here. *(Adds to Part 9 / North Stars.)*

## 12.2 Law 6 (The Critique's Permanent Addition)

> **Law 6 — Buttery or it didn't ship.**
> Every scroll is 60fps. Every Replay plays instantly and never stutters. Every transition is frame-perfect. The promise of "premium" is broken by a single hitch. Performance is not optimization work done at the end; it is a feeling we owe the user in every frame, and it has veto power over any feature that can't meet it.

---

## Appendix A — One-Page Summary

- **What it is:** the movie, the story, and the companion of your life — a product that makes you fall in love with your own existence and helps you become more of who you want to be.
- **Soul:** Reverence, Revelation, Return. Comparison-with-self, never others. Lead with emotion, support with data.
- **IA:** Home · Timeline · ◉Replay · Stories · You — plus an omnipresent AI Companion.
- **Hook:** the Genesis Replay (60-second wow) → daily themed Replays + "This Day, Every Year" → the gated Life Replay as lifetime crown.
- **Moat:** the Biographer/Companion intelligence + a privacy-first, anti-surveillance trust contract + a coherent, emotionally-specific design language (Aurora).
- **Growth:** export beautiful cinematic artifacts (not an in-app social feed); the annual Year Replay as a Wrapped-beating cultural moment.
- **Money:** free is genuinely complete; Premium ($79.99/yr) unlocks the full Life Replay, unlimited generation, fidelity, voice Companion, deep Insights, clean sharing; Legacy adds family archives and permanence. Never paywall the soul.
- **The 10:** stop being passive — help people *become*, prove the change, have the range and courage to tell the whole truth of a life, and obsess over the one quotable daily magic. A relationship with your own life. People don't churn out of that.

*End of document.*












