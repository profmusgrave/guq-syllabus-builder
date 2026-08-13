# GU-Q Syllabus Builder

A single-file web tool for Georgetown University in Qatar faculty to build compliant, customizable syllabi for AY 2026–27.

**Use it here:** https://profmusgrave.github.io/guq-syllabus-builder/

## What it does

- **GU-Q calendar built in.** Fall 2026 and Spring 2027 term dates, the Sunday–Thursday week, Fall break, Sports Day, Eid al-Fitr, Easter Sunday, and registrar key dates are hardcoded. The tool knows that Monday, January 4, 2027 runs on a Sunday schedule and handles it for you.
- **Schedule generation.** Pick your meeting days (U/M/T/W/R) and get a week-by-week schedule with holidays skipped and swap days flagged.
- **Exam planning.** Midterm dates chosen from your actual class meetings; final exam dates chosen from the official exam windows, with validation.
- **Policy library.** Every course policy area (AI, attendance, participation, collaboration, deadlines, communication, technology and wearables, recording, virtual attendance, continuity, office hours) offers CNDLS-vetted sample language selected by stance, editable, and linked back to the authoritative CNDLS page. University-mandated blocks (Honor Code, ARC, Title IX, support services) are always included.
- **Consistency checks.** Participation policy and grading weights are cross-checked; grading totals are validated.
- **Outputs.** Full syllabus as Markdown (paste into Word or Google Docs), a one-page quickstart handout, an `.ics` calendar file importable into Canvas/Google/Outlook, and a structured `.json` course shell for downstream tools.

## Data and privacy

All data stays in your browser (localStorage). Nothing is transmitted anywhere. Clearing your browser data clears your saved syllabus, so download your outputs when done.

## Verify before publishing

Policy sample language was captured from CNDLS pages at build time. Always follow the ground-truth links inside the tool to confirm current approved university language before distributing a syllabus.

## Adapting for another campus or year

Everything campus-specific lives in a few constants near the top of the `<script>` block in `index.html`:

- `TERMS` — term dates, holidays, key dates, and schedule-swap days
- `EXAM_WINDOWS` — official exam periods
- `POLICY_DEFS` / `MANDATORY_DEFS` — policy stances and university boilerplate

Fork, edit those, done.
