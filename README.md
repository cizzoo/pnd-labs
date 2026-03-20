# pnd-labs all for one

> [!CAUTION]
>
> Please DO NOT push your solutions to the master branch. Create a branch with your nickname and push your solutions to that branch. This way, we can keep the master branch clean and organized.

This repo contains solutions to the labs for the PND course from different users. 

> [!CAUTION]
>
> Do I really need to say that this is NOT an official repo for the course? This is just a repo where students can share their solutions to the labs. The solutions in this repo are not guaranteed to be correct | complete or the best solution ever created. Use them at your own risk.

## Usage

> [!WARNING]
>
> If you already have a local copy of the original repo with your solutions, and you want to push your solutions to this repo, jump to this section: [Push your solutions](#push-your-solutions-from-existing-local-copy).

### First time

1. Fork or clone (if you have write access) this repo.
2. Create a branch with your nickname and start solving the labs in this branch.

```bash
git checkout -b <your-nickname>
```
3. Finally, commit and push your solutions to this branch.

### Push your solutions (from existing local copy)

> [!WARNING]
>
> If you already followed the steps in the previous section, you can skip this section.

If you already have a local copy of the original repo with your solutions, you can push your solutions to this repo by following these steps:

0. [__original repo__] Commit your solutions to your local copy of the original repo if you haven't already.

1. [__original repo__] Add this repo as a remote to your local copy of the original repo with your solutions:

```bash
git remote add pnd-labs https://github.com/cizzoo/pnd-labs.git
```

2. [__original repo__] Push your solutions to this repo:

```bash
git push pnd-labs master:<your-nickname> # we want a branch for each user, so we push to a branch named after your nickname
```

3. [__this repo__] Pull the changes from this repo to your local copy of this repo:

```bash
git fetch origin
git checkout <your-nickname>
git pull
```

---

# pnd-labs
Kathara labs for Practical Network Defense course at Sapienza

Further details for the Kathara environment: https://github.com/KatharaFramework

Further details for the course: https://sites.google.com/di.uniroma1.it/practical-network-defense
