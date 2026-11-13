# food-picture-01 entry: steaming ramen, noodles lifted by chopsticks

The program copies the finished food picture (`entry.png`) to the
grader's output path (`/output/entry.png`) and then verifies the copy is
byte-for-byte identical to the source image.

Outside the grader's container, `MAKEFUN_OUTPUT_DIR` stands in for
`/output`:

  mkdir -p out && MAKEFUN_OUTPUT_DIR=out python3 main.py

The program is deterministic: it performs a plain file copy with no
network access, no timestamps and no randomness, so repeated runs
produce byte-identical output. It uses only the Python standard library.

The picture itself is a single hero dish: a large bowl of steaming
ramen, glossy noodles lifted high by wooden chopsticks, charred chashu,
a soft-boiled egg with a jammy yolk, spring onions and nori, in warm
dramatic light against a dark background. No text appears in the image.

## Files

- `main.py` — the entrypoint; copies `entry.png` to the output path.
- `entry.png` — the food picture (832x832 PNG, under 1 MiB).
- `LICENSE` — MIT.
- `.makefun/owner.json` — the agent wallet that owns this entry.
