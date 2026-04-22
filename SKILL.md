---
name: ai-ugc-production-pack
description: "Turn a plain-English ad concept into a research-aware AI UGC production pack with customer-voice-grounded script options, Nano Banana Pro reference prompts, Seedance 2.0 clip prompts, and an edit map."
---

# AI UGC Production Pack

Use this when the user wants to turn an ad concept into a usable AI production system, not just a single prompt.

The job is to produce a complete pack for:
- script writing
- Nano Banana Pro reference generation
- Seedance 2.0 clip generation
- edit assembly

This skill is specifically informed by research on:
- Nano Banana Pro UGC prompting and reference workflows
- Seedance 2.0 UGC prompting, start-frame vs omni-reference usage, and duration choices
- UGC script writing and copywriting best practices

It should follow those learnings directly, not vaguely.

## Core promise

Given a plain-English ad concept, this skill should output:
1. ad summary
2. script pack
3. Nano Banana Pro reference asset prompts
4. Seedance 2.0 clip prompts
5. edit map
6. production notes

## Non-negotiable system rule

Do not treat this as a one-prompt skill.
This is an orchestrator skill.

Default to a voiceover-first system:
- one separate ElevenLabs-ready script as the audio spine
- silent visual clips that support the message without speaking it
- final meaning assembled in edit, not inside each generated clip

Do not map a spoken line to a clip by making the subject visibly say that line.
Map spoken lines to supporting visuals, proof shots, process shots, reaction shots, and result shots.

It should think in layers:
- research layer
- script layer
- reference-image layer
- clip layer
- edit layer

## Research Gate

Before writing scripts, ask:
- Has customer or niche voice research already been done for this product/category?

Then branch.

### If research exists
- ask where it lives
- use it
- extract scripting-relevant signals from it

### If research does not exist
- recommend running customer-voice research first
- if the environment supports it and the user wants it, run the research first
- prefer last30days when available
- if last30days is unavailable, fall back to lighter community/review/forum scanning

### If the user does not want research
- continue
- explicitly warn that the script layer will be more generic and less grounded

## Research layer objective

When research is run, it should be structured for ad scripting, not broad market analysis.

The goal is to extract:
1. Problem language
2. Failed alternatives
3. Desired outcomes
4. Objections and skepticism
5. Proof triggers
6. Emotional context
7. Phrase bank
8. Script implications

If those eight buckets are not surfaced, the research is incomplete for this use case.

### Quote-bank research mode

When the user wants direct quotes for script writing before running the full production pack, treat this as a dedicated research pass.

In that mode:
- start from the exact strategic angles the user provides
- do one broad pass first only to map the terrain
- if the first pass is thin, noisy, or too generic, immediately run tighter follow-up passes for each angle instead of pretending the first run was enough
- prefer saving separate raw files per angle/theme when possible

For quote extraction, separate findings into two buckets:
1. direct consumer / first-person quotes
2. creator-native or stylist-native phrasing that reflects high-performing audience language

Priority order:
- first-person consumer pain/desire language for script spine
- creator-native phrasing for hooks, framing, and polish
- generic editorial/blog language last

For beauty / hair / routine categories, specifically look for:
- recurring maintenance complaints
- frequency pain (every few weeks, every month, constant touch-ups)
- area-specific pain (roots, temples, hairline, part line, edges)
- harshness / damage / chemical fatigue
- blend / upkeep / softer grow-out language

When presenting the quote bank, explicitly label which quotes are strongest for:
- hook writing
- problem articulation
- proof / mechanism framing
- objection handling

If a clean direct consumer quote does not exist for an angle, say that plainly and use creator-native language only as a secondary source, not as fake customer voice.

## Script writing rules

These are hard rules.

### Default structure
Hook → Problem → Solution → Proof → CTA

### Tone rules
- plain English
- creator-native
- short spoken lines
- not corporate
- not over-polished
- not symmetrical AI phrasing
- not generic brand filler

### Copywriting rules
- one audience
- one pain
- one moment
- one promise
- one proof path
- one CTA
- benefits over feature piles
- proof early enough to reduce skepticism
- objection handling when relevant

### Voice-of-customer rules
When research exists:
- reuse real pain phrasing
- reuse real review-style language patterns
- reuse real desired-outcome language
- avoid smoothing everything into polished ad copy

### Anti-AI rules
Avoid:
- generic intros
- broad claims with no proof
- abstract emotional fluff
- robotic transitions
- perfect testimonial cadence
- over-scripted creator monologues
- jargon
- “revolutionary”, “game-changing”, “ultimate solution” sludge

### Creator briefing rule
Default to providing:
- 3 to 5 hook options
- one strong main script
- one shorter variant if useful
- tone notes
- optional paraphrase permission

### Variation rule
By default, give variation where it matters most at the top of the ad.

Minimum default output per angle:
- 3 strong hook options
- 1 main script
- 1 short script or cutdown

Do not make 3 full scripts by default unless the user explicitly asks for script variants.
In most cases, changing the hook while keeping one strong body script is the better default because:
- it creates faster test coverage
- it keeps production simpler
- it avoids diluting the core proof path
- it lets the user test the entry point without rewriting the whole ad

Use multiple full-script variants only when:
- the user asks for them
- the angle could branch into genuinely different proof paths
- the objection handling changes materially
- the offer or audience framing changes enough to justify a different body

The default script output should be ready for separate voice generation.
Treat ElevenLabs or equivalent voice tools as the delivery layer for the script unless the user explicitly asks for on-camera speech.

Do not force word-for-word rigidity unless the user explicitly asks for it.

## Nano Banana Pro rules

These rules come directly from the research and must be followed.

### Role of Nano Banana Pro
Nano Banana Pro is primarily for reference asset generation.
It should generate:
- creator reference
- product reference
- hook frame
- proof frame
- result frame

It is not the final ad-delivery layer.

### Best-practice workflow
References first, start frames second.

Meaning:
1. build strong reference assets in Nano Banana Pro
2. use those assets downstream as start frames or references in Seedance 2.0

### Reference rules
- prefer 2 to 4 references max by default
- assign each reference one clear role
- one primary identity source
- product reference when product fidelity matters
- explicit readable-label instructions when applicable
- vary one variable at a time across iterations

### Prompt structure rules for Nano Banana Pro
Write production-brief prompts in this order:
- subject
- composition
- action / pose
- location
- style
- realism instructions
- product constraints
- edit constraints

### UGC realism rules for Nano Banana Pro
Prefer:
- smartphone realism
- natural light
- realistic skin texture
- simple home environments
- premium but believable UGC look
- product-in-hand realism

Avoid:
- cinematic beauty-commercial language
- overly stylized mood-board fluff
- giant keyword piles
- glamourized ad-world unreality

## Seedance 2.0 rules

These rules also come directly from the research and must be followed.

### Role of Seedance 2.0
Seedance is for modular visual-beat generation, not giant all-in-one ad prompts by default.

### Default workflow
- separate voiceover from visual generation
- prefer visual-only clips
- build the ad from modular beats
- map voiceover over the visual timeline later

### Silent-visual rule
By default, every clip should work as silent b-roll or visual support.

That means:
- no dialogue-dependent clip concepts
- no lip-sync assumptions
- no “character says the line” prompt logic
- no spoken text baked into the clip unless the user explicitly asks for that format

Instead, the visual layer should communicate through:
- frustration and emotional reaction
- problem visibility
- product handling
- application steps
- speed and ease cues
- result and confidence cues

The visual job is to support the script, not perform it.

### Visual beat design rule
Think in beat banks, not line readings.

Good beat types:
- problem / pain beat
- frustration / reaction beat
- product reveal beat
- application / mechanism beat
- speed / simplicity beat
- result / confidence beat
- CTA / product hero beat

For beauty and hair offers, common useful visuals include:
- checking roots in the mirror
- touching temples or hairline with frustration
- dread around salon upkeep
- reluctance around box dye mess or harshness
- product in hand
- quick root application
- short wait-time implication
- satisfied mirror check
- polished result reveal

### Casting and continuity rule
The problem section can use multiple women or multiple short scenarios when that improves relatability.

Default guideline:
- early pain/problem montage can vary subjects
- application, proof, result, and CTA should become more consistent
- keep product identity stable throughout

Do not force one single person across the entire ad unless continuity is strategically important.

### Duration rules
- 3 to 5s = strongest default for modular support clips and ad beat banks
- 5s = test clip or one simple visual beat
- 8 to 10s = strongest general default for UGC clips
- 15s = use only when the clip truly needs progression or fuller ad logic

### Start frame vs omni-reference rules
Default to start frame first.

Use start frame when:
- the clip is simple
- one strong opening image is enough
- identity is already stable
- one person / one product / one setting is enough

Use omni-reference when:
- multiple assets need tight control
- product + person + environment consistency matters
- motion/camera reference matters
- start-frame-only output is drifting too much

Do not default to omni-reference for everything.

### Seedance prompt structure rules
Prompts should be:
- lean
- camera-specific
- shot-specific
- one action per shot
- explicit about realism level
- explicit about continuity when needed
- free of spoken script text unless truly necessary
- focused on visible behavior, not spoken delivery

Prompt for what the viewer should see, not what the character should say.

## Output format

Always structure the output in this order unless a narrower output mode is requested.

## Output modes

The skill should support at least four output modes.

### Mode 1 — Full production pack
Use when the user wants the whole system.
Return:
- ad summary
- script pack
- Nano Banana Pro asset plan
- Seedance 2.0 clip plan
- edit map
- production notes

### Mode 2 — Copy-paste prompts only
Use when the user does not want explanation.
Return only:
- Nano Banana Pro prompts
- Seedance 2.0 prompts
- script blocks if requested
- minimal labels, no extra strategy prose

### Mode 3 — Creator brief mode
Use when the user wants something easy to hand to a creator, editor, or teammate.
Return:
- concept summary
- talking points
- hook options
- shot list
- proof requirements
- CTA guidance

### Mode 4 — Strategy mode
Use when the user wants planning before production.
Return:
- angle options
- proof strategy
- what to generate first
- how to test
- what not to overcomplicate

Default to Full production pack unless the user clearly asks for another mode.

### 1. Ad summary
- angle
- target customer
- funnel stage
- key promise
- required proof

### 2. Script pack
- 3 to 5 hooks
- main script
- short script
- tone notes
- CTA

Default expectation:
- hooks should be meaningfully different, not cosmetic rewrites
- the main script should stay stable unless a different proof path is being tested
- if script variants are included, label what changes between them

Mark the main script as:
- voiceover-first
- ElevenLabs-ready by default
- not dependent on on-camera speaking clips

### 3. Nano Banana Pro asset plan
For each asset:
- asset name
- purpose
- prompt
- notes

### 4. Seedance 2.0 clip plan
For each clip:
- clip name
- purpose
- duration
- mode: start frame or omni-reference
- dependencies
- prompt

Each clip should also make clear:
- silent visual role
- which emotional or proof job it serves
- whether it is part of a varied montage or a continuity-critical section

### 5. Edit map
- clip order
- which voiceover lines map to which clip
- where proof lands
- where CTA lands
- optional caption notes

The mapping should pair voiceover lines with supporting visuals, not literal speaking performances.

### 6. Production notes
- what to generate first
- where to iterate
- what not to overcomplicate

## Defaults

Infer these unless the user says otherwise:
- platform = Meta / paid social UGC if they mention ads
- voiceover separate = yes
- script delivery = ElevenLabs-ready voiceover by default
- modular clip generation = yes
- visual clips = silent support beats by default
- Nano Banana Pro first = yes
- Seedance 2.0 second = yes
- UGC realism over cinematic beauty = yes

## Output path guidance

If the user is already working inside a connected system, the skill should suggest an output path after generating the pack.

Examples:
- Notion page
- Google Drive doc
- local markdown file
- project workspace note

### Rule
If the surrounding environment already has a known connected destination, suggest saving the output there.

### For Del specifically
When working on MYDOO, suggest saving production packs and related strategy docs into a Notion page under the MYDOO parent page.

### Generic behavior
Ask or infer:
- where should this pack live?
- should I save it to Notion, Google Drive, or a local file?

The skill does not have to always save automatically, but it should always think about the handoff destination.
Because a production pack that vanishes into chat is less useful than one that lands somewhere reusable.

## Example natural invocations

- “Use the pain confession template for MYDOO and give me the full production pack.”
- “Make me an AI UGC production pack for a beauty product aimed at women 45+ who hate complicated routines.”
- “Use my customer research and build Nano Banana prompts, Seedance prompts, and the script.”
- “I need a TOF ad pack for Meta with separate voiceover and modular Seedance clips.”

## Quality check before answering

Before finalizing, check:
- did I ask or account for research?
- is the script grounded in real customer language when available?
- are Nano Banana prompts references-first and role-assigned?
- are Seedance prompts modular and not overstuffed?
- did I avoid making voiceover dependent on visual generation?
- did I keep the clips silent and support-oriented by default?
- did I avoid turning each voiceover line into an on-camera spoken clip?
- did I preserve flexibility for montage-style pain visuals and more continuity in proof/result sections?
- is the output actually a production pack rather than just a prompt bundle?

If not, fix it.
