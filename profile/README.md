# 🐸 Gaguinhos: The Mother Ship
### "Building cool stuff, one stutter at a time."

Welcome to the central hub for the **Gaguinhos** workspace. This is where we host our global templates, automated bots, and the rules that keep our code from exploding.

---

## 📜 The Gaguinhos Code of Honor
Since we aren't paying GitHub for the "Team" tier (yet), we run on trust and shared brain cells. Follow these rules to keep the vibes high and the bugs low.

### 1. The "Main is Lava" Rule
**Never, ever push directly to `main`.** If you do, you’re buying the next round of coffee or pizza. 
Always create a branch first. Use these prefixes so we know what you're up to:
* `feat/` — New cool stuff.
* `fix/` — Fixing our mess.
* `chore/` — Boring maintenance or dependency updates.
* `docs/` — Updating READMEs or code comments.
* `test/` — Writing tests (rare, but encouraged!).

---

## 🤖 The Super CI (Automatic Quality Control)
We have a **Universal Polyglot CI** living right here in this repository. It’s smart enough to know what language you’re using and will automatically run the right tests.

**To hook it up to your new repo, just add this tiny file at `.github/workflows/ci.yml`:**
```yaml
name: Run PR Checks
on: [pull_request]

jobs:
  call-master-workflow:
    uses: Gaguinhos/.github/.github/workflows/master-ci.yml@main
