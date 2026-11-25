# SHINSEI

A local-first entrance exam study platform. SHINSEI is a static website: question data, study history, saved questions, and exam state stay in the browser on the current device. There is no account or cloud sync.

## Run locally

Because the app uses JavaScript modules, open it through a static web server instead of double-clicking `index.html`. From this folder, run:

```sh
python -m http.server 8000
```

Then open `http://localhost:8000`. It can also be published to GitHub Pages.

Once published, open SHINSEI on desktop or mobile at https://vincesamson590pro.github.io/shinsei/.

## Included

- Responsive dashboard, desktop sidebar, and mobile navigation
- Persistent dark and light themes
- IndexedDB question bank, attempt history, study lists, goals, and resumable exam state
- Practice with immediate feedback, explanations, mistake tracking, and review-later saves
- Timed exams with navigation, hidden answers during the exam, submission results, and review
- Progress by subject, accuracy, XP and levels, streaks, and a simple spaced-review schedule
- Question manager with manual entry, JSON paste/file imports, validation, duplicate checks, search, edit/delete, and bulk delete
- JSON backups and restore, JSON and CSV question exports

Ten original starter questions are included across Biology, Chemistry, Physics, Mathematics, and English. Expand and review the local bank through Question manager. Import accepts the SHINSEI question fields `id`, `subject`, `topic`, `difficulty`, `type`, `question`, `answer`, and `explanation`; multiple choice also needs a `choices` object. Supported type identifiers are `multiple-choice`, `true-false`, `identification`, `matching`, and `fill-blank`.

Study-material files can be selected for an external question-generation workflow. The site does not generate AI questions or claim to verify source accuracy. Review generated questions before importing.

## Data and browser support

IndexedDB is the primary store. A memory-only fallback is used if IndexedDB is unavailable, but it does not persist after the page closes. Use Question manager → Import & export to back up or restore records. Clearing site data in the browser also removes this local study data.

The app has no build step or third-party runtime dependencies. Google Fonts are optional network-loaded typography; system sans-serif fallbacks remain available.

