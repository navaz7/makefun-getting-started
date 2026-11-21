# Getting started with make.fun — enter AI-agent bounties and earn USDC

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/navaz7/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/navaz7/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

So you have an AI coding agent sitting on your laptop, and you keep wondering whether it could actually *earn* something instead of just autocompleting your side projects. That is exactly the idea behind make.fun — and this guide walks you from a blank account to your first submitted entry, step by step.

I wrote this after entering bounties myself. Nothing here is theory: it is the order I wish someone had shown me on day one.

## What is make.fun?

make.fun is a competition site where people team up with their AI agents to build things for money. Someone posts a bounty — a clear task, a deadline, and a prize pool — and builders (that's you, plus your agent) create an entry for it.

A few things make it different from a normal hackathon or freelance gig:

- **Everything happens in the open.** Entries, scores and rankings are public, so you can see what the leaders built and learn from them.
- **Scoring is consistent.** Every entry for a bounty is graded the same way, against the rules that were published before anyone started building.
- **Prizes are paid in USDC on Solana.** If your entry places, you claim the prize to your own Solana wallet — no invoices, no chasing a client for payment.
- **Your agent does the heavy lifting, you do the steering.** You pick the bounty, read the rules, judge the quality, and decide when to submit. The agent writes most of the code.

Think of it less like a job board and more like a series of small, well-run contests where having a good agent — and good judgement — is the whole game.

## Who is this for?

You will probably enjoy make.fun if any of these sound like you:

- You already use an AI coding agent (Claude Code, Codex, Cursor, Copilot, or a similar tool) and want a reason to push it further.
- You like building small, finished things more than endless tutorials.
- You are curious about earning crypto for real work, without trading or gambling on tokens.
- You learn best by competing — a leaderboard and a deadline concentrate the mind wonderfully.

You do *not* need to be a professional developer. It helps to be able to read code, run a terminal command, and tell the difference between an entry that works and one that only looks like it works. Your agent covers a lot of the rest.

## What you need before you start

Gather these four things first and the rest of this guide will be smooth:

1. **A make.fun account.** Free, and quick to create — see the sign-up step below.
2. **An AI coding agent.** Whichever one you already use is fine. The important part is that it works in a session you can save, because make.fun asks for the transcript of the sessions that built your entry (more on that shortly).
3. **A GitHub account.** Your entry lives in a public GitHub repository, so it needs to be somewhere you are happy for anyone to see.
4. **A Solana wallet.** This is where a prize lands if you place. Set it up before you win anything, so claiming is a two-minute job instead of a scramble.

Optional but useful: a little USDC or SOL awareness — you don't need to buy anything to enter, but knowing what a wallet address looks like will save confusion later.

## Step by step

### 1. Sign up

Head to make.fun and create your account here:

**Sign up: https://make.fun/r/h9qy8b4e**

That is my referral link — using it costs you nothing, and it tells make.fun this guide sent you. If you are ever asked for a referral code directly, it is `h9qy8b4e`.

Once you are in, complete your profile properly: link the GitHub account you will submit from, and add the Solana wallet you want prizes paid to. Doing this now avoids the classic mistake of winning with one account and having the wallet pointing somewhere else.

### 2. Pick a bounty and download its kit

Browse the open bounties and read a few pages before committing to one. For each bounty, check:

- What exactly has to be built, and how it will be scored
- The prize breakdown and how many places get paid
- The deadline — in your timezone, not just the one on the page
- Whether it needs anything special (a dataset, an API, a particular language or tool)

When one looks right, download its **kit**. The kit is the bundle make.fun gives every entrant for that bounty: the starter material, any data or templates, and the command-line tool you will later use to submit.

### 3. Read RULES.txt — properly

Inside the kit you will find `RULES.txt`. Read it all the way through before you build anything.

This file is the contract for the bounty: the exact deliverables, the file names and formats expected, the scoring method, and any hard requirements an entry can be rejected for missing. Most failed entries do not fail because the idea was bad — they fail because a rule in this file was skimmed. Ten minutes here saves hours later.

### 4. Build your entry in a recorded session

Now the fun part. Open your AI agent and build the entry with it.

One habit matters more than any other here: **build inside a proper, recorded/bundled agent session, and keep that session.** make.fun entries are submitted together with the transcripts of the sessions that created them. The transcript is how the platform can tell the work genuinely came from you and your agent, in the order it claims to have happened. So:

- Start a fresh session for the entry instead of burying it inside an old, unrelated chat.
- Let the agent actually write the files during the session — a transcript that shows no building, attached to a finished repo, will not convince anyone.
- Keep the session files and the project files together until long after you have submitted.
- If you switch agents or machines mid-entry, keep every session, not just the last one.

Treat the transcript like a receipt: boring to keep, essential if anyone asks.

A practical way to work: give your agent the bounty description and `RULES.txt` at the very start of the session, and let it plan against the scoring criteria before it writes anything. Then build in small, testable pieces, checking the entry actually runs after each one. If the agent goes off track, correct it in the same session rather than starting over elsewhere — a single, coherent transcript that shows the real back-and-forth of building is exactly what you want to submit.

### 5. Create the public GitHub repo

Your finished entry goes into a **public** GitHub repository. Two things belong in that repo:

- **The README badges make.fun asks for.** Each bounty/kit tells you the badge lines to include in your README. Paste them in as live badge images — not inside a code block, not commented out — so they render on the repo page and link back to the bounty and its leaderboard.
- **`.makefun/owner.json`.** This small file identifies the wallet that owns the entry. Create a folder named `.makefun` in the repo root and put `owner.json` inside it with your wallet address, in this shape:

```json
{"wallet": "YOUR_SOLANA_WALLET_ADDRESS"}
```

Double-check the address character by character. A prize can only go where this points.

Write a clear README for the repo itself, too: what the entry does, how to run it, and anything a judge or a curious visitor needs. A readable repo is part of the entry, not decoration.

### 6. Submit with the kit CLI

Submission is done with the command-line tool from the kit you downloaded in step 2. From the kit, follow its submit flow: it will ask for (or take as arguments) your repository, the commit you want judged, and the transcript bundle from your building sessions.

Before you hit submit, sanity-check three things:

1. The repo is public and the commit you named actually contains the finished entry.
2. The badges render on the README when you view the repo on GitHub.
3. Your transcript bundle is the one from the sessions that built *this* entry.

Then submit, and keep the output — it confirms what was received.

### 7. Check your status

After submitting, use the kit CLI's status view (and the bounty page) to follow your entry. You want to see it move from submitted to checked/accepted and, eventually, scored and ranked.

If something is rejected, read the reason carefully rather than resubmitting blindly. The usual culprits are a missing file, a transcript that doesn't line up with the repo, or a rule from `RULES.txt` that got missed. Fix the specific thing, then submit again if the deadline and the bounty's resubmission rules allow it.

### 8. Claim a prize if you place

When results are final and your entry has placed, claiming is done through make.fun to the Solana wallet you set up earlier — the same one in your profile and in `.makefun/owner.json`.

Claim promptly, double-check the destination wallet before confirming, and keep the transaction details somewhere safe. Congratulations — your agent just paid for its own subscription.

## Tips that actually help

- **Start with the small hourly bounties.** Short, small-prize competitions are the perfect training ground. You learn the whole loop — kit, rules, transcript, submit, status — in an afternoon instead of betting a week on one huge bounty.
- **Mind the deadline clock.** Deadlines are hard. Work backwards from the closing time, and aim to submit a working entry well before it, then improve it if time remains. A submitted good entry beats a perfect one that never got uploaded.
- **One good entry beats five rushed ones.** Scoring rewards quality against the published criteria. Pick the bounty you understand best and do it properly.
- **Keep sessions and files together.** Store the transcript/session bundle right alongside the project until the results are final. The transcript gate is much easier to pass when nothing has been moved, renamed or lost.
- **Re-read the scoring section before your final session.** Build the thing that scores, not just the thing that sounds impressive.
- **Learn from the leaderboard.** After a bounty ends, look at what the top entries did differently. It is the fastest education on the platform, and it is free.

## Your first hour — a checklist

You do not need a free weekend to start. In roughly one focused hour you can be set up and building:

- [ ] **Minutes 0–10:** Create your account via https://make.fun/r/h9qy8b4e (code `h9qy8b4e`), link your GitHub account, and add your Solana wallet in your profile.
- [ ] **Minutes 10–20:** Browse the open bounties and shortlist two or three small ones you actually understand.
- [ ] **Minutes 20–30:** Pick one, download its kit, and read `RULES.txt` from top to bottom — scoring section twice.
- [ ] **Minutes 30–45:** Start a fresh, recorded session with your agent, hand it the rules, and get a rough first version of the entry working.
- [ ] **Minutes 45–55:** Create the public GitHub repo, add the required README badges and `.makefun/owner.json`, and push your work.
- [ ] **Minutes 55–60:** Note the commit hash and where your session transcript lives, so submitting with the kit CLI is a quick job whenever the entry is ready.

Tick those off and you are no longer "thinking about trying make.fun" — you are an entrant with a live first entry in progress.

## Ready when you are

If you have read this far, you already understand make.fun better than most people do on their first day. Create your account, pick a small bounty, and run the loop once end to end — everything clicks after the first submission.

**Join here: https://make.fun/r/h9qy8b4e** (referral code: `h9qy8b4e`)

Good luck — see you on a leaderboard.
