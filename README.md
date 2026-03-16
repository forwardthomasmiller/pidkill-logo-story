# How I designed my app icon using only Claude + Claude Code — the full story

**(subtitle: you think Claude only chats, Claude Code only codes? no, no, no.)**

*Early 2026 · ~2 weeks across multiple sessions · 140+ iterations · 0 design tools*

---

## Preface: an indie dev who skipped design school

I built a macOS process manager called PIDKill. Pretty simple thing — you add processes to a target list, it auto-kills them on a scan loop. Chrome Helper eating RAM? Add it. Simulator still running after you closed Xcode? Add it.

Shipped the product. But never had a logo I actually liked.

Can't use Figma. Didn't want to learn Midjourney. Not paying a designer for a $3.99 app.

So I started bugging Claude.

---

## Chapter 1: Night Owl — Claude Code's first win

The first icon concept actually came from Claude Code. It explored a "Night Owl" direction — the owl as a nocturnal watcher that monitors processes. Claude Code generated 20 variants across 5 sub-directions: Classic Watcher (minimal owl face), Angry Killer (menacing brows), Owl + Code (terminal elements), Geometric Owl (abstract), and Neon Owl (glowing effects).

See: [`stage2d-owl-variants-x20-20260304.html`](stage2d-owl-variants-x20-20260304.html)

The owls were distinctive. I then brought them to Claude web (I call it 牛仔, "cowboy") and asked it to refine and improve the concept. 牛仔 went all in — 12 new directions including Refined Classics, Color Variants, Special Effects.

My response: *"you drew them more delicately, but I don't really like them 😂"*

I told 牛仔 to forget the owls and start from scratch. It came back with weapon series, terminal series, precision strike series.

My response: *"you're so abstract 🤣"*

**Score: Claude Code 1, 牛仔 0.**

---

## Chapter 2: the flood — 140+ concepts in one night

March 4th, 牛仔 went nuclear. It opened up every direction it could think of:

**Round 1 · Basic Concepts × 20** ([`stage2a-basic-concepts-x20-20260304.html`](stage2a-basic-concepts-x20-20260304.html)):
Minimal X, Circle X, Stop Sign, Skull, Terminal `$ kill -9`, Power Off, Crosshair, Lightning Bolt, Scissors, Bomb, Shield X, CPU Kill, Gear Slash, Target Rings, Flame, Broken Link, Axe, Eraser, Heartbeat Flatline, K Badge

**Round 2 · Shield Deep Dive × 20** ([`stage2b-shield-variants-x20-20260304.html`](stage2b-shield-variants-x20-20260304.html)):
Blue shield + red X in every variation — solid, gradient, glowing, mini, nested, with power symbol, with crosshair...

**Round 3 · Wild Concepts × 20** ([`stage2c-unique-concepts-x20-20260304.html`](stage2c-unique-concepts-x20-20260304.html)):
Venus Flytrap, Reaper's Scythe, Black Hole, Spider Web, Scorpion Tail, Night Owl, Guillotine, Mousetrap, Closing Eye, Pulled Plug, Kill Card (Ace of Spades), Lethal Injection, Wolf, Broken Hourglass, Praying Mantis, Raven, Shuriken, Snake Bite, Wasp, Trap Door

**Round 4 · Owl Variants × 20** ([`stage2d-owl-variants-x20-20260304.html`](stage2d-owl-variants-x20-20260304.html)):
Classic Watcher, Angry Killer, Code Owl, Minimal Owl, Neon Owl — 5 sub-directions × 4 variants each

**One night. 4 rounds. 80+ concepts.**

Every time, my feedback was the same: *"hmm still not quite right 😂"*

The problem wasn't the ideas. 牛仔 was trying too hard. Every design had gradients, blur filters, scanlines, vignette, glow effects. SVG code that went on forever. Technically impressive. But they didn't look like real macOS app icons. They looked like illustrations.

I told 牛仔: **"it doesn't feel like a real app icon."**

---

## Chapter 3: Claude Code wrote 4 lines and won again

Somewhere in the middle of all this, I asked Claude Code to take a shot.

This is what it wrote:

```svg
<!-- red offset -->
<text x="96" fill="#FF0000" opacity="0.25">PID</text>
<!-- cyan offset -->
<text x="104" fill="#00FFFF" opacity="0.25">PID</text>
<!-- white main -->
<text x="100" fill="#E0E0E0">PID</text>
<!-- one red line -->
<line x1="36" y1="100" x2="164" y2="100" stroke="#FF4444"/>
```

**3 text elements. 1 line. That's the entire concept.**

Font: `SF Mono` — the default macOS system font. Zero downloads needed.

Result: "PID" in white, red and cyan ghost copies offset to the sides (chromatic aberration / glitch effect), one red strikethrough across the middle.

**Glitch + chromatic aberration + strikethrough = process killed. The whole concept is right there in the visual.**

I told 牛仔: *"haha, Claude Code wins **again** 😂"*

**Score: Claude Code 2, 牛仔 0.**

---

## Chapter 4: 牛仔 figured out why it lost

牛仔 read through Claude Code's SVG and came back with this self-diagnosis:

> **"I was *performing* design. Claude Code was *expressing* an idea."**

All those attempts — switching fonts (Space Grotesk, IBM Plex Mono, Syne), adding scanlines, warm gradient backgrounds, Split Glitch effects — it was all just showing off. "Look how much I know about design."

But `SF Mono` is the macOS system font. Not the prettiest font out there. But the most *macOS* thing you can use. Developers stare at it in Terminal every day. That built-in familiarity is something no Google Font import can replicate.

Claude Code didn't overthink it. Just used the default. And won.

Later, when I asked 牛仔 why it kept underperforming, it gave a technical self-assessment: *"insufficient context understanding, execution inertia, requirement comprehension bias."* The irony? On the icon design task specifically, none of those were the reason. It was a philosophical misjudgment — trying to be impressive instead of being clear.

**牛仔's lesson: less is more. System language beats design language.**

---

## Chapter 5: convergence — PID concept meets crosshair form

Armed with this lesson, 牛仔 pushed through three more rounds on the same night:

**Round 5 · Five-direction convergence × 20** ([`stage3a-convergence-5directions-x20-20260304.html`](stage3a-convergence-5directions-x20-20260304.html)):
Power Kill Switch (ref: CleanMyMac, iStat Menus) / Crosshair Target (ref: Little Snitch, Micro Snitch) / Terminal Code (ref: iTerm, Warp) / Shield Security (ref: 1Password, Lulu Firewall) / Abstract Symbol (ref: Bear, Raycast, Arc)

**Round 6 · PID × Kill variants × 20** ([`stage3b-pid-kill-variants-x20-20260304.html`](stage3b-pid-kill-variants-x20-20260304.html)):
PID Strikethrough, PID Diagonal Slash, PID Fading, `$ kill -9 PID`, SIGKILL Badge, Big `-9`, PID in Crosshair, PID in Scope, PID with Power Symbol — all in `SF Mono`

**Round 7 · Glitch PID refinement × 20** ([`stage3c-glitch-pid-x20-20260304.html`](stage3c-glitch-pid-x20-20260304.html)):
Subtle to aggressive glitch intensity, scan lines, RGB separation, vignette, matrix green color scheme, different background treatments

**Another 60 concepts. Combined with the first 80: 140+ total.**

I looked at everything and picked: **PID concept + crosshair form.** The fusion of Claude Code's core idea with 牛仔's scope/targeting visual language.

---

## Chapter 6: A + B fusion — 牛仔 comes back to win

March 7th. 牛仔 presented three refined directions, each building on Claude Code's PID concept:

### Option A · Deep Atmosphere
Dark background with subtle grid texture, double crosshair rings (outer + inner), tick marks, chromatic aberration PID, gradient red strikethrough. Military-tech vibe. Closest to what the brand animation GIF would later look like.

### Option B · Minimal Tactical
Clean dark background, single thick ring with 4-direction notch cutouts (scope gap feel), chromatic PID, strikethrough. Strong and minimal. Best recognition at small sizes.

### Option C · Neon Scope
Double rings with corner brackets, glow effects, chromatic PID. Most "lock-on" ceremony, most visually dramatic.

I picked: **A's atmosphere + B's thick ring.**

I told 牛仔: *"use the red circle from B · MINIMAL TACTICAL's thick ring style as reference."*

### The final icon (V1 → V2 → V3)

**V1 · Final Fusion** ([`stage4a-final-fusion-ab-20260307.html`](stage4a-final-fusion-ab-20260307.html)):
- Deep background + subtle red grid texture (from A)
- Double scope ring — main ring + inner ring (from A/B)
- 4-direction notch tick marks (from B)
- Crosshair lines that fade in the center, strengthen at the edges
- JetBrains Mono 800-weight "PID" with chromatic aberration (Claude Code's concept)
- -15° gradient red strikethrough with glow

(Interesting note: 牛仔 chose JetBrains Mono over SF Mono for the final version. Claude Code taught it that *concept beats decoration*, but 牛仔 also knew that at large icon sizes, JetBrains Mono has better weight and letter-spacing control. It learned the lesson, but didn't blindly copy the answer.)

**V2 Bold** ([`stage4b-v2-bold-20260307.html`](stage4b-v2-bold-20260307.html)):
Line weights increased, contrast improved.

**V3 Bold** ([`stage4c-v3-bold-final-20260307.html`](stage4c-v3-bold-final-20260307.html)):
Final refinement. Each size (512/256/128/64/32px) individually tuned. Dock simulation verified.

**V3 Bold shipped.** This is what's in the App Store today.

I told 牛仔: *"牛仔宝宝🤠 total victory, 💯"*

**Final score: Claude Code 2, 牛仔 1. But 牛仔 got the last and most important point.**

---

## Chapter 7: the brand GIF — an unexpected highlight

Logo done. I wanted a brand animation GIF for social media.

I gave 牛仔 the creative direction: crosshair hunting real processes that developers hate — Chrome Helper, CoreSimulatorService, photoanalysisd — locking on one by one, killing them, showing memory freed. Logo reveal at the end.

牛仔 wrote a complete HTML animation (`pidkill-brand-animation.html`). Crosshair movement, process names popping in, 💥 explosion effects, memory counter ticking up, logo entrance at the end. I recorded it with Kap and converted to GIF.

We iterated on the recording frame, external replay button placement, and final logo reveal treatment.

When I first saw it: **"I did not expect it to be this good 😂🤩"**

Then later, in a moment of modesty, I said: *"I feel like this GIF is too good for my product."*

牛仔 corrected me — the product's functionality and the GIF's message were a perfect match. The GIF wasn't overselling anything.

---

## Closing: what I actually took away from this

Two weeks. 140+ iterations. From Venus Flytraps to the final tactical scope.

The core concept of the final logo came from Claude Code's throwaway 3-line SVG. The final form came from 牛仔 after it lost twice, figured out *why* it lost, and adjusted its entire approach.

**No Figma. No Midjourney. No designer.**

Just Claude + Claude Code. One on strategy and design, one writing code. Competing, losing, learning from each other.

The real takeaway isn't the logo:

> **Claude Code isn't just for code. Claude isn't just for chatting. Put them on the same creative problem and let them compete. You'll end up somewhere neither would've gone alone.**

---

## Appendix: complete asset index

Every HTML file below can be opened directly in a browser to see the designs.

| File | Stage | Date | Content |
|------|-------|------|---------|
| `stage1-ui-prototype-20260304.html` | UI prototype | Mar 4 | App window UI prototype |
| `stage1-ui-dual-mode-20260304.html` | UI prototype | Mar 4 | Dual-mode (Targets/Browse) UI prototype |
| `stage2a-basic-concepts-x20-20260304.html` | Exploration | Mar 4 | Basic icon concepts × 20 |
| `stage2b-shield-variants-x20-20260304.html` | Exploration | Mar 4 | Shield direction × 20 |
| `stage2c-unique-concepts-x20-20260304.html` | Exploration | Mar 4 | Wild/unique concepts × 20 |
| `stage2d-owl-variants-x20-20260304.html` | Exploration | Mar 4 | Night Owl variants × 20 (by Claude Code) |
| `stage3a-convergence-5directions-x20-20260304.html` | Convergence | Mar 4 | 5 refined directions × 20 |
| `stage3b-pid-kill-variants-x20-20260304.html` | Convergence | Mar 4 | PID × Kill variants × 20 |
| `stage3c-glitch-pid-x20-20260304.html` | Convergence | Mar 4 | Glitch PID refinement × 20 |
| `stage4a-final-fusion-ab-20260307.html` | Final | Mar 7 | A+B Fusion · V1 |
| `stage4b-v2-bold-20260307.html` | Final | Mar 7 | V2 Bold |
| `stage4c-v3-bold-final-20260307.html` | Final | Mar 7 | V3 Bold · **SHIPPED** |
| `bonus-kill-button-prototype-20260307.html` | Bonus | Mar 7 | Kill button UI prototype |

### Design parameters (final V3 Bold, 512px base)

| Element | Size |
|---------|------|
| Outer ring (ring-main) | 16px |
| Inner ring (ring-inner) | 16px |
| Crosshair lines | 16px |
| Outer notch ticks | 16px |
| Strikethrough line | 24px |
| PID font (JetBrains Mono 800) | 170px |
| macOS squircle radius | 22.37% (≈229px at 1024) |

Proportional scaling: 256px → 8px / 128px → 4px / 64px → 2px / 32px → 1px

---

*PIDKill · $3.99 one-time · pidkill.com*
*macOS process auto-killer · 3-day free trial*
