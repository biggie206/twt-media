# The 1-Page Architecture of My Auto-Posting Stack
*The exact system behind @build.withtom + @tech_withtom — two faceless IG pages that post daily with ~10 minutes of human review. Total software cost: $0/month.*

```
 4:58am  SCOUT (Claude scheduled task)
         researches the niche → writes spec.json + reel.json
            │
 7:10am  BUILDER (launchd job on a Mac mini)
         renders branded slides + reel from the spec
         (Python + PIL + ffmpeg — no Canva, no subscriptions)
            │
 ~8:00am HUMAN GATE (the only manual step)
         review the preview grid → fix or approve
            │
         QA GATE (script)
         checks specs, captions, duplicate phrases, media mix
            │
         PUBLISH (Meta Graph API — free, official)
         carousel + reel, wrong-account safety stop
            │
         DM BOT (every 30 min, Graph API private replies)
         "Comment WORD" → sends the promised resource
            │
 Sunday  ANALYTICS (script)
         non-follower reach, saves, sends → next week's experiment
```

## The 6 pieces & what they replace
| Piece | Built with | Replaces |
|---|---|---|
| Scout | Claude scheduled task | a content researcher |
| Builder | Python + PIL + ffmpeg | Canva Pro / a designer |
| QA gate | ~200-line Python script | proofreading mistakes at 11pm |
| Publisher | Meta Graph API (free) | Buffer/Later ($15-80/mo) |
| DM bot | Graph API private replies | ManyChat ($29-139/mo) |
| Analytics | Graph API insights | guessing what worked |

## The 3 rules that make it work
1. **Spec-driven, not vibe-driven.** The scout writes a JSON contract; the builder renders it identically every time. Change the spec schema once, every future post inherits it.
2. **One human gate, everything else automated.** You review a preview grid with your coffee. That's the job.
3. **Steer by non-follower reach + sends** — not follower count. A weekly script pulls the numbers; one experiment per week.

## Want this for your page?
This exact stack is what I use daily — every post you see on @build.withtom came out of it. I'm packaging it up; if you'd want it for your own page (or your business's), reply **STACK** to the DM and tell me what page you'd run it on. Early access goes to the first replies.

— Tom (@build.withtom · @tech_withtom)
