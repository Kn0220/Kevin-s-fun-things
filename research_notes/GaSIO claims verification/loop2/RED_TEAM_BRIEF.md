# Loop 2 — red-team brief

You are the adversary of loop 1. Loop 1 produced a verdict per claim (files in ../loop1/). Your job is to try to **overturn or sharpen** each verdict, not to confirm it. Read PROTOCOL.md (../PROTOCOL.md) for the framework and the claims, then the loop-1 file(s) for your groups.

## Rules
1. For every claim, state the strongest case that loop 1 is WRONG, then test it with at least one new search or fetch. Record the result even when it fails.
2. Run the loop-1 "Gaps for loop 2" / "NOT RUN (budget)" queries for your groups first — they are the known blind spots.
3. Search budget is shared across the team and limited (~60 WebSearch calls each). Prioritise; prefer `WebFetch` on known URLs (free of the search budget). If a host is blocked, try `https://web.archive.org/web/2025/<url>` or `https://r.jina.ai/<url>` once before giving up, and log the attempt.
4. Grade evidence with the protocol's L1–L6 levels. A primary page you actually opened outranks a search extract of the same page.
5. Separate three things in every write-up: (a) what the CCS document literally says, (b) what independent evidence shows, (c) what CCS probably meant (typo, different basis, different model). (c) is a hypothesis, label it so.
6. Output per claim:
```
### <ID>
**Loop-1 verdict:** … (confidence …)
**Red-team case:** the best argument that loop 1 is wrong
**Test:** <query/fetch> → <result, source, level>
**Outcome:** UPHELD / OVERTURNED / SHARPENED — new verdict, new confidence, one-line reason
**Settling document CCS could provide:** …
```
End with: a "Verdict changes" table (ID | loop-1 | loop-2 | why), "Primary sources opened" list, "Still unresolved" list for loop 3.
