# WORDLY. — Vocabulary Checking Studio

> Vibrant Learning Arcade × Teacher-led classroom assessment · Vietnamese / English

**Status:** Project initialized. Awaiting the **approved WORDLY 2.0 Google Stitch export** before implementing any visual UI. **Do not reuse the discontinued WORDLY V1 design.**

## Project purpose

WORDLY is a bilingual, teacher-led English vocabulary checking and progress-tracking web application for Vietnamese high schools (Global Success, grades 10, 11 and 12). Teachers operate live sessions on a projector; students do not need personal devices.

## Source-of-truth and development workflow

1. **Google Stitch:** approved visual designs, exported HTML/CSS, screenshots, assets and DESIGN.md.
2. **ChatGPT Plus:** implement functional React + Vite from those approved designs; preserve layout, typography and visual assets.
3. **GitHub:** work directly in this repository; implement on feature branches with PR reviews before production release.
4. **Vercel:** build/test previews and deploy reviewed changes.
5. **Supabase:** authenticated persistent storage with row-level security. No real student records before authorization and security verification.
6. **BRIAN:** integrate after the standalone application is validated.

**No Codex. No Google AI Studio. No AI features or API calls inside WORDLY.**

## Required product scope

- **Home:** launch class sessions, recent sessions, review cues.
- **Global Success Library:** grade 10–12, ten units per grade; teacher-verified word records with POS, meanings, examples, optional IPA, media, collocations and word forms. Do not fabricate textbook word lists.
- **Vocabulary Manager:** add/edit/delete, draft → reviewed → published, import/export CSV/XLSX, duplicate detection, validation.
- **Classes:** import rosters, stable student IDs, class/student management and attendance eligibility.
- **Session Builder:** select class, multiple units, verified words, challenge modes, question count, time limits and picker rules.
- **Challenge Modes:** meaning flip, reverse recall, word scramble, missing letters, picture guess, context challenge, collocations, word formation, listen/spell, hint reveal, speed round and mixed. Enable modes only when their reviewed source data exist.
- **Fair Student Picker:** random without replacement within a round; exclude absent students; teacher override and explicit priority-review mode.
- **Classroom Live:** 16:9, large visual prompts, projector privacy controls, answer reveal, timers, audio when available, pause/resume, keyboard shortcuts, skip and undo.
- **Scoring:** teacher-controlled Correct (2), Partially Correct (1), Not Yet (0); absent, skipped and unassessed are separate from score zero. Maintain audit history for score corrections.
- **Session Summary:** participation, attempts, error patterns, retry candidates and teacher notes.
- **Student Growth:** repeat attempts, comparable-assessment trends, 7/14-day retention checks and per-word history.
- **Class Insights:** participation coverage, challenge results, difficult items, teacher-entered instructional adjustments and follow-up results.
- **Report Studio:** student/class/session reports, printable A4 PDF, CSV/XLSX export, Vietnamese/English/bilingual versions.
- **Settings:** VI/EN UI, timer/scoring defaults, reduced motion, audio, accessibility, backup and restore.

## Visual requirements

- The latest approved Google Stitch design is the **single source of truth** for layout, typography, colors, spacing, illustration, graphics and component states.
- **Vibrant Learning Arcade**: colorful, sophisticated gamified EdTech, energetic 2.5D illustrations, large challenge cards, expressive graphical feedback and restrained motion; visually playful without feeling childish.
- **Do not use the retired Editorial/Scholarly Editorial aesthetic**, magazine serif styling, ivory/forest-green identity, or the discontinued WORDLY V1 assets.
- Suggested palette (subject to approved Stitch design): Electric Blue #4865F5, Coral #FF6B6B, Teal #14C6B4, Sunshine #FFCC47, Violet #9167F2, Midnight Navy #17233D, Cloud #F7FAFF.
- Prefer friendly rounded sans-serif typography, such as Be Vietnam Pro and Nunito Sans, with strong Vietnamese diacritic support.
- Minimize prose in teacher workflows without hiding required functions; generous touch targets and high-contrast 16:9 projector views.
- Use visual cards, large illustrated challenges, animated student picker, progress rings and attractive, readable learning charts; avoid meaningless decoration.
- Distinct Teacher Workspace and immersive **Classroom Live**.
- Accessible large screen / iPad use, keyboard navigation, reduced motion.
- Centralized static VI/EN translation resources; no automatic AI translation at runtime.

## Data and security principles

- Demo data must be visibly marked **DEMO**.
- No claims of learning improvement without comparable recorded evidence.
- Class/student records accessible only to authorized teacher accounts.
- Supabase RLS and server-side authorization for recording grades / protected answer keys.
- Never expose secret/service-role keys or student personal data in repository or deployment previews.

## Development stages

1. Stitch visual fidelity and VI/EN foundations.
2. Verified vocabulary repository, class roster and imports.
3. Session Builder, student picker and Classroom Live challenge engine.
4. Session history, corrections, learner growth and reports.
5. Supabase security, integration tests and production readiness.
6. Controlled integration into BRIAN.

> Next input: export ZIP from **new** Google Stitch WORDLY 2.0 project (all screens, HTML/CSS, assets, and DESIGN.md where available). This repository intentionally contains no replacement visual design yet.
