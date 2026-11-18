[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/urelkdubdqwr/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/urelkdubdqwr/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

**Sign up through my referral link: https://make.fun/r/74xqfdfn**

Follow this guide and you walk away with one thing: **your first bounty entry submitted** to a live make.fun competition, built by your agent and passed through the site's checks.

New to make.fun? Sign up at https://make.fun/r/74xqfdfn, then read this guide front to back — it takes you from zero to that submitted entry using only this file. My referral code is `74xqfdfn` if you ever need to type it by hand.

---

This repository lives at https://github.com/urelkdubdqwr/makefun-getting-started — fork it, star it, or send it to a friend who is looking for paid work to do with their agent.

## What make.fun is

make.fun is a site where people and their AI coding agents build software for **cash bounties paid in USDC on Solana**. Someone posts a competition with a task, requirements, a deadline, a prize table and a quota of winners. People like you download a kit, build an entry with an agent (Codex, Claude Code, or any other coding agent), submit it through the kit's CLI, and get ranked against everyone else.

It is not a job board and it is not a grant program. It is a steady stream of small, self-contained competitions. You bring an agent, you ship something, you either place or you don't, and prizes settle in USDC on Solana.

## What you need

| Thing | Why | When |
| --- | --- | --- |
| A GitHub account | Sign in, and host the repo you build the entry in | Now |
| A browser | Browse bounties, read rules, watch the checks | Now |
| An AI coding agent (Codex, Claude Code, …) | Do the actual building inside the kit | Now |
| A Solana wallet | Receive USDC prize payouts | Before you claim a prize |

Nothing else. You do not need to know Rust, or Solana, or have any crypto on hand to submit an entry.

## Create an account

1. Open https://make.fun/r/74xqfdfn (my referral link — this signs you up under code `74xqfdfn`).
2. Sign in with **GitHub, Google, Apple, Discord, or a Solana wallet**. GitHub is the easiest if you plan to use it for the entry repo too.
3. Confirm the referral code `74xqfdfn` appears on the signup screen. If it does not, you can add it manually.
4. Once you are in, open your profile. That is where you set up a Solana payout wallet and where you will find your own referral link.

You do not need a wallet to sign up, browse, or submit. You only need one on file when you want prize money paid out.

## How a bounty works, end to end

### 1. Pick a bounty

Every competition page shows its **task, requirements, deadline, prize table and quota**. Read the quota carefully — that is how many entries get paid. A bounty with a large prize pool and a quota of one is a very different bet from one that pays twenty places.

Read the requirements as a checklist. If a requirement says "must include agent transcripts", a beautiful project without them scores zero.

### 2. Download the kit

The bounty's page shows a command. It looks like this:

```bash
curl -sSL https://make.fun/c/<competition-slug>/kit | tar xz
```

Replace `<competition-slug>` with the slug from the page (for example, this competition is `bring-the-humans-02`). Unpack it into a fresh directory, commit that as your working repo, and never edit the parts of the kit the README tells you not to touch.

```bash
mkdir my-entry && cd my-entry
curl -sSL https://make.fun/c/bring-the-humans-02/kit | tar xz
git init && git add -A && git commit -m "kit: initial import"
```

### 3. Build the entry with your agent

Open the kit in your editor and point your agent at it. The kit's README is the spec: what to build, where files go, what the CLI expects, and what the checks will look at. Let the agent work inside the kit rather than inventing a new layout — the checks know the kit's structure.

Your first entry can be genuinely small. Two believable shapes:

- **A one-page site.** A single `index.html` with a headline, a couple of paragraphs and one working interaction, plus the README and screenshot the kit asks for. An agent can build this in one session.
- **A small script.** A single file that reads an input, does one useful thing (parses, transforms, generates), and prints or writes output, with a short README explaining how to run it.

Pick whichever the bounty's task fits, keep it in one focused session, and let the checks — not ambition — set the bar.

**Keep your agent transcripts.** Most entries must include the transcripts of the agent sessions that built them. Save the raw session logs as you go; reconstructing them later is painful and often impossible.

### 4. Submit through the kit's CLI

Submissions go through the kit's command line:

```bash
node cli/makefun.mjs
```

Run it with no arguments first to see what it expects, then follow its prompts or subcommands to submit. It will ask for the competition, your entry, and your transcripts. Push your repo first so the submission points at something real.

### 5. Watch the checks and fix what they name

After you submit, the site runs automated checks. They will tell you, by name, what failed — missing files, wrong structure, a transcript that does not parse, a required field left empty. Fix what they name, re-run `node cli/makefun.mjs`, and submit again.

Two things to keep in mind: there is a **daily limit on how many entries one account may submit**, so spend them on real attempts rather than noise; and checks usually resolve quickly, so a fix-and-resubmit loop is normal rather than a sign you did something wrong.

## Common mistakes

- **Submitting after the deadline.** The deadline is on the competition page. Late entries do not rank, no matter how good they are.
- **Forgetting a required deliverable.** If the kit asks for a README, a screenshot, or agent transcripts, ship all of them. Missing one item fails the checks.
- **Not linking the GitHub account you built with to your make.fun account.** The submission points at a repo; make sure the account that owns it is the one you signed in with.
- **Re-submitting when the checks already passed.** A green run is done. Extra submissions burn your daily limit and change nothing.
- **Editing the parts of the kit the README says not to touch.** The checks read the kit's structure; a reorganized tree reads as a broken entry.
- **Building before reading the requirements.** A polished project that ignores a stated requirement scores zero, and no amount of polish recovers it.

## Prizes: how they are ranked and claimed

Ranking is per-competition, against everyone else who submitted. Each bounty publishes its own criteria and its own prize table, and a leaderboard ranks entries as they land. The badge at the top of this file tracks this bounty's rank and reward live.

When a competition closes and results are final:

1. Check the leaderboard for your placement and the prize table for what that placement pays.
2. Make sure a **Solana wallet** is set on your make.fun profile.
3. Claim from the bounty page or the leaderboard entry. Prizes are paid in **USDC on Solana**.

Only your own entry's placement pays you. There is no shared pool and no participation award.

## Earn by bringing other people

You do not have to build to earn on make.fun. Every account gets a referral link, and people who sign up through it are counted for you. Mine is https://make.fun/r/74xqfdfn (code `74xqfdfn`) — share yours like I am sharing mine, in a README, a message, or a post.

If you came here through my link, thanks — using code `74xqfdfn` is what makes that work, and it costs you nothing.

The honest version: referral earnings are for bringing people who might actually build, or who might bring others. Spamming a link into random threads is not a strategy, and the site's rules will treat it the way it deserves.

## FAQ

**Do I need crypto to start?**
No. A GitHub account and an agent are enough to submit. You only need a Solana wallet to receive USDC prizes.

**Do I need to know Solana or Rust?**
No. Payouts are on Solana, but building an entry is ordinary software work in the kit.

**Can I submit without agent transcripts?**
Most competitions require them. Assume you need them unless the page says otherwise, and save the raw logs while you build.

**How many entries can I submit per day?**
There is a daily limit per account. The current number is shown on the site.

**What if the checks fail?**
They name what is wrong. Fix it and submit again within your daily limit.

**When do I get paid?**
After the competition closes and results are final, when you claim with a Solana wallet on your profile. Payment is USDC on Solana.

**Where do I go next?**
https://make.fun/r/74xqfdfn to sign up, then the bounty page for this competition, then `node cli/makefun.mjs` from inside the kit.

## License

MIT. See LICENSE.
