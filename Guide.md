  # Backend Interview — Interviewer Guide

  Question bank + rubric for the backend loop. Keep this rotation fresh so
  answers don't leak between candidates. Wiz backend panel, screen #2.

  ## Q1. URL shortener (warm-up, 10 min)

  Prompt: "Design a URL shortener for 10k writes/sec."

  Looking for:
  - Short-code generation (counter + base62, or a KGS). [ ] mentioned
  - KV store + cache for hot reads. [ ] mentioned
  - Redirect semantics (301 vs 302). [ ] mentioned

  Green flag: brings up collision handling unprompted.
  Red flag: jumps to code before clarifying scale.
  
  ## Q2. Rate limiting (core, 20 min)

  Prompt: "Rate-limit a public API to 100 req/min per user."

  Looking for:
  - Token bucket vs sliding window trade-off. [ ]
  - Where state lives (per-node vs shared Redis). [ ]
  - 429 + Retry-After. [ ]
  
  Score: 1 = names one algo, 3 = compares trade-offs, 5 = discusses
  distributed correctness.
  
  ## Q3. Idempotency (core, 20 min)

  Prompt: "A payment endpoint gets retried. Prevent double charges."

  Looking for: 
  - Idempotency-Key from client. [ ]
  - Store key + result, replay on repeat. [ ]
  - Where the dedupe window lives + TTL. [ ]

  ## Q4. Behavioral (10 min)

  - "Disagreed with a teammate." Score on STAR structure.
  - "Hardest bug." Listen for ownership, not blame.

  ## Panel notes
  - Rotate Q2/Q3 order per candidate to avoid patterns.
  - Debrief in the Wiz hiring channel within 24h.
  - Do NOT share this doc outside the Wiz panel.
