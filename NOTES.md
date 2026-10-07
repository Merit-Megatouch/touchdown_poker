# TOUCHDOWN POKER (touchdown_poker)

Status: **runs (smoke-tested)** — starts, renders and reacts to taps headless; not yet played by hand. Scaffolded 2026-10-07. Facts: [notes/scaffold.md](notes/scaffold.md).

## Checklist
- [ ] Window size in game.conf matches the largest PNG (notes/scaffold.md)
- [ ] Every symbol in notes/unresolved.txt has a stand-in in src/host/loader_services.cpp
      (`make analyze GAME=touchdown_poker` until it reports 0)
- [ ] First run: `make run GAME=touchdown_poker DEBUG=shots` — crash trace + screenshots in notes/shots
- [ ] Paths: `make run GAME=touchdown_poker DEBUG=files`; engine trace: `mkdir -p data/var/merit/debug/files && touch data/var/merit/debug/files/resource_locator`
- [ ] Reference code: `make decompile GAME=touchdown_poker`
- [ ] Translations + help text appear (gamedata/translations/touchdown_poker.utf8)
- [ ] Sound and music play (`DEBUG=sound`)
- [ ] A full game plays through (`DEBUG=profile` to catch stalls and old-malloc bugs)

## Log
<!-- dated notes: what broke, what fixed it -->
- 2026-10-07 — smoke test 2026-10-07: tools/smoke.sh runs 25 s headless with taps; no crash, screens render (build/smoke/touchdown_poker). 
