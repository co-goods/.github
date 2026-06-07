# Co-Goods Contributor License Agreement (CLA)

This folder holds the Co-Goods CLA. Contributing to any Co-Goods repository requires agreeing to it. You sign **once** — a single signature covers your contributions across **all** Co-Goods repositories.

- **Current version:** [`cla-v1.md`](./cla-v1.md)
- **Signatures:** recorded in [`CLA-SIGNATURES.md`](../CLA-SIGNATURES.md)

## How to sign

You agree to the CLA by adding one row to `CLA-SIGNATURES.md` in a pull request. The row format is:

```
| Your Name | @your-github-handle | v1 | YYYY-MM-DD |
```

How you open that pull request depends on whether you have write access to the repository.

### If you don't have write access (most contributors)

You can't push a branch to a repository you don't have write access to, so your pull request comes from your own **fork**. The easiest path needs no local setup:

1. Open [`CLA-SIGNATURES.md`](https://github.com/co-goods/.github/blob/main/CLA-SIGNATURES.md) on GitHub.
2. Click the **pencil (Edit)** icon. GitHub automatically creates a fork for you.
3. Add your row to the bottom of the signatures table.
4. Click **Commit changes…**, then **Propose changes** — this opens a pull request from your fork back to `co-goods/.github`.

Prefer the command line? Fork the repo on GitHub, then:

```bash
git clone https://github.com/<your-handle>/.github.git co-goods-dotgithub
cd co-goods-dotgithub
git switch -c sign-cla
# add your row to CLA-SIGNATURES.md
git commit -am "docs: sign CLA"
git push origin sign-cla
# then open a pull request on GitHub
```

You can also fold your signature into the **same** pull request as your actual contribution — just add the `CLA-SIGNATURES.md` row there (this works when your contribution is to `co-goods/.github`; for other repos, sign here first).

### If you have write access (core team)

No fork needed — branch directly:

```bash
# from a clone of co-goods/.github, on an up-to-date main
git switch -c sign-cla
# add your row to CLA-SIGNATURES.md
git commit -am "docs: sign CLA"
git push origin sign-cla
# then open a pull request
```

We never commit straight to `main` — always branch and open a pull request.

## What happens next

A maintainer reviews and merges your signature pull request. Once merged, you're covered for all Co-Goods repositories and don't need to sign again (unless we publish a new CLA version, in which case signing again is optional and we'll say so). As the project grows we'll automate this with a CLA assistant on each pull request; until then, the manual row is the record.
