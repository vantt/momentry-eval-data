# momentry eval data (private)

The eval set of [momentry](https://github.com/vantt/momentry): copies of real agent transcripts, the owner's labels, paid model captures and measurement results. It holds raw session text that never went through momentry's privacy check, so it lives in its own private repo, apart from the code, and is not shared with the coding agents.

## Where it goes

Clone it into the momentry checkout at `docs/_private/eval` (that path is gitignored by momentry):

```sh
cd momentry
make eval-data        # clones this repo there, or pulls if it is already there
```

Every command in momentry's `scripts/eval/README.md` and `docs/development.md` then works as written, for example `go run ./cmd/momentry-eval run --manifest docs/_private/eval/manifest.json` (replay, 0 USD).

## What is here

- `manifest.json`: the eval sessions; transcript and label paths are relative to this folder.
- `transcripts/`: copies of the source transcripts, so the set survives the agents' own transcript cleanup.
- `labels/`: the owner's labels per session (`status: reviewed` when checked).
- `<session id>/runs/`: paid captures, replayed for free.
- Named folders (`new-defaults/`, `not-a-story/`, …): captures and results of one experiment each; the write-up is in momentry's `docs/experiments/`.
- `results/`: summary of each harness run.

Commit label edits and new captures here, then push; code changes go to momentry.
