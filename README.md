[README.md](https://github.com/user-attachments/files/34352401/README.md)
# Personal OS — Modular Domain Engine

## GitHub repository structure

```text
personal-os/
├── index.html
└── domain/
    ├── money.html
    ├── fitness.html
    ├── game.html
    ├── writing.html
    ├── speaking.html
    ├── upskilling.html
    └── projects.html
```

## Upload instructions

1. Download and extract this ZIP.
2. In your GitHub repository, replace the existing `index.html` with this `index.html`.
3. Upload the complete `domain` folder (all seven HTML files) beside `index.html`.
4. Commit the changes to the `main` branch.
5. Open the deployed site and test each Domain Area.

**Important:** Keep the `domain` folder beside `index.html`. Do not upload it inside another nested folder. GitHub Pages must be able to resolve paths such as `./domain/game.html`.

## What changed

- The main application shell remains in `index.html`.
- Each Domain Area now has its own HTML fragment under `domain/`.
- Selecting a Domain Area loads its fragment into the shared workspace.
- The existing Game weekly tracker markup is moved to `domain/game.html`.
- The existing Game JavaScript, CSS, Supabase integration, authentication, and data operations remain in `index.html` to minimize risk in this first extraction.
- The other six modules are starter fragments. Their current generic placeholder experience is preserved; their individual interfaces can now be developed in their own HTML files.
- Personal Engine, Productivity Engine, and Life Engine have not been intentionally redesigned or restructured.

## Notes

- Serve the application through GitHub Pages or another HTTP server. Opening `index.html` directly as a `file://` URL may block `fetch()` requests.
- The browser-safe Supabase URL and publishable key remain where they were in the supplied source. Never place a Supabase service-role/secret key in client-side code.
