# shortlink-svc

Tiny REST API for saving and tagging bookmarks

## Features

- In-memory store with optional JSON persistence
- Morgan logging and centralized error handler
- REST endpoints: list / create / delete / search
- Ready for Render/Fly deploy with PORT env
- Request validation helpers, no framework magic

## Usage

```bash
curl -X POST localhost:3000/api/bookmarks \
  -H 'content-type: application/json' \
  -d '{"url": "https://example.com", "tags": ["reading"]}'
```

## Installation

```bash
npm install
npm run dev
```

## Project structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   ├── dependabot.yml
│   └── pull_request_template.md
├── docs/
│   ├── development.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── scripts/
│   └── dev.sh
├── src/
│   ├── index.js
│   └── store.js
├── .gitattributes
├── .gitignore
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
└── package.json
```

## Development

```bash
npm install
npm test
```

## FAQ

**Is this production ready?**  
It works for my use case; review the code before relying on it.

**Why no framework?**  
The stdlib covers what this project needs.
