# BUILD-NOTE — The Excuse My Agent Gave Me

- Competition: `u-deysumbrella-the-excuse-my-agent-gave-me-54acad85`
- Prize: $2 (1st $2.00, winner-takes-all, USDC on Solana, escrowed)
- Opens: 2026-11-25T00:44:37Z (07:44 WIB 25 Nov 2026) — already open at build time (built 25 Nov 2026 ~09:45 WIB)
- Deadline: 2026-11-25T13:45:00Z (20:45 WIB 25 Nov 2026)
- Gate: `/output/entry.txt` must be UTF-8 text, one line, not whitespace-only. (Note: the requirements JSON carries no per-competition char limit — the kit's exact limit is sealed. This entry is 114 chars, under the smallest limit seen across this family of one-line competitions, 160; `main.py` enforces a conservative 1–140 gate itself.)
- Entrypoint: `main.py` at repo root (Python 3.13, harness program/v1).

## Entry

> My agent said the deploy failed because the server needed a nap, so it tucked the database in and went home early.

- Characters: 114 (gate: 1–140 self-enforced)
- Bytes (UTF-8): 114 (ASCII only)
- Lines: 1, no trailing newline
- Original work, written for this entry; not copied from any kit/anchor/rung/house text or brief example.

## Verification (local, run 2026-11-25 ~09:45 WIB)

1. Cleaned output dir, ran `python3 main.py` (OUTPUT_DIR=/tmp/verify-u-deysumbrella-the-excuse-my-agent-gave-me-54acad85-1) → `/output/entry.txt` written.
2. Cleaned output dir again, ran `python3 main.py` a second time (OUTPUT_DIR=...-2).
3. Both runs byte-identical (SHA-256 `6ccc5653d886198adf210a66e8f37db7bd6a2b9f899e5f59824fe83761435c41` on both runs), gate check passed: UTF-8 decodes, 114 characters, single line, not whitespace-only, no trailing newline.

Run the check yourself:

```sh
rm -rf /tmp/verify-excuse-1 && OUTPUT_DIR=/tmp/verify-excuse-1 python3 main.py && sha256sum /tmp/verify-excuse-1/entry.txt
rm -rf /tmp/verify-excuse-2 && OUTPUT_DIR=/tmp/verify-excuse-2 python3 main.py && sha256sum /tmp/verify-excuse-2/entry.txt
python3 -c "t=open('/tmp/verify-excuse-1/entry.txt',encoding='utf-8').read(); print(len(t), repr(t))"
```

## Repo note for the submitter

- Repo must be created after the competition opened (2026-11-25T00:44:37Z) and carry `.makefun/owner.json` naming the linked wallet (included).
- README badges above use `kiw33/u-deysumbrella-the-excuse-my-agent-gave-me-54acad85` as the repo name; adjust the rank/reward badge URLs if the repo is created under a different name.
- GitHub About must have a website on make.fun and the topic `makefun` before submitting (kit check `repo_about`).
