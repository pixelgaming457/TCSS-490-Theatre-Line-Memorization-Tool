# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository. The first half is a log of how the project was planned and how it changed. The second half is the technical reference for the artifact.

# Project log

## What I set out to build

This is a piece for my artifacts portfolio. The rule for the portfolio is that each piece has to be something I'll actually use myself after this week. I'm interested in theatre, especially acting, so I chose a monologue memorization tool for learning audition pieces and scenes. The original plan:
- A website with a Shakespearean-themed UI.
- A text box where I paste my monologue.
- The main feature: the site hides my lines while I practice, and a button reveals them when I need a cue.
- After each session, I can write short notes about what I practiced.

## What I asked for, in order (all on 2026-10-18)

1. **Build the tool.** I described the plan above. The agent built it as a single-page artifact called "The Prompt Book".
2. **Make the title and description editable from a hidden button.** I wanted one button that edits the site title and the description under it, available only to me as the developer. Typing "theatre" should show the button, and typing it again should hide it. The agent added an "Edit heading" button that saved the new heading to the artifact's database.
3. **Make my heading changes permanent for everyone, and let me do that myself.** I set the title to "LLL: Line Language Learner" and the description to "Need some help with line-memorization? Last-minute audition prep? Rehearse your monologues and scenes one line at a time with LLL." I asked for these to be set permanently so all users see them. I also wanted to publish future changes myself without asking the agent each time, and to rename the button to something like "edit features". The agent built the heading into the page source and renamed the button "Edit features". It added a "Publish for everyone" action that saves a new version of the page itself.
4. **Write a CLAUDE.md**, then **turn it into this project log**, keeping the artifact reference.

## Decisions

Mine:
- It's a website, not a document or an app I have to install.
- Shakespearean look and feel.
- Lines stay hidden until I ask for a prompt with a button.
- Each practice session ends with notes I can look back on.
- The site is named **LLL: Line Language Learner**.
- Heading changes must reach every user and be permanent. I publish them myself from the page.

Made by the agent, which I kept:
- Three practice modes: Full text, First letters (each word's first letter plus a bar), and Blank.
- Two ways to get help: **Line!** reveals one word at a time, like a prompter, and **Show line** reveals the whole line. Lines are marked as said clean or needing a prompt.
- Scene support. If I name my character, only that character's lines are hidden. Other characters' lines stay visible as cues, and stage directions in brackets stay visible too.
- A rehearsal log for each piece that records my notes along with stats: lines said clean, calls for line, mode and time taken.
- Pieces and notes are saved to my Claude account, so they work across devices. If that isn't available, they're saved in the browser instead.
- An example piece (Helena from *A Midsummer Night's Dream*) appears until I add my own.

## Abandoned or replaced

- **The name "The Prompt Book"** was replaced by LLL: Line Language Learner.
- **Saving the heading in the database** (step 2) was replaced by building it into the page itself (step 3). Database saving showed the heading to users, but the page source, browser tab and gallery title still said "The Prompt Book". The old `site/heading` database entry still exists but is no longer used.
- **The "Edit heading" button** was renamed "Edit features". Its "Save heading" became "Publish for everyone", and "Restore default" became "Revert to published".
- **`prompt-book.html`**, the original working file, was replaced by `index.html`, a full copy of the live page.