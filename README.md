# neural-ghost
Official Neural Ghost project repository for AI &amp; tech content, branding, and digital assets
# create project folder
mkdir neural-ghost
cd neural-ghost

# initialize git
git init
git branch -m main

# create README and basic files
cat > README.md <<'EOF'
# Neural Ghost 👻🤖

Faceless AI & tech media: short-form tech news, reels, carousels, and deep dives.
EOF

# sample .gitignore
cat > .gitignore <<'EOF'
node_modules/
dist/
.env
.DS_Store
*.log
EOF

# initial commit
git add .
git commit -m "Initial commit: README and .gitignore"

# link to GitHub (replace YOUR_USER)
git remote add origin git@github.com:YOUR_USER/neural-ghost.git
git push -u origin main
mkdir -p branding/logo branding/animation branding/color-palette content/instagram content/reels content/carousels scripts/ai-news website/src website/public .github/workflows
touch LICENSE CONTRIBUTING.md CODE_OF_CONDUCT.md
# Neural Ghost 👻🤖

**Neural Ghost** — faceless AI & tech media.

## What’s inside
- `branding/` — logos, color palettes, animations
- `content/` — Instagram captions, reel scripts, carousels
- `scripts/` — tools to fetch/summarize AI news (ethical)
- `website/` — static website for long-form content

## Contributing
See `CONTRIBUTING.md`.

## License
MIT
git add README.md
git commit -m "Update README with Neural Ghost overview"
git push
cat > LICENSE <<'EOF'
MIT License
Copyright (c) 2025 Neural Ghost
Permission is hereby granted...
EOF
git add LICENSE
git commit -m "Add MIT license"
git push
**Hook (1 line):**  
[Bold, curiosity-piquing sentence]

**Explanation (2-3 short paragraphs):**  
- What happened
- Why it matters
- Quick take / implication

**CTA:**  
Follow @NeuralGhost for daily AI & tech updates.

**Hashtags:**  
#AI #MachineLearning #NeuralGhost #TechNews
00:00 - Hook (3s)
00:03 - Quick explanation (10s)
00:13 - Visual / code snippet (7s)
00:20 - Final takeaway & CTA (5s)
git add content/
git commit -m "Add Instagram caption and reel templates"
git push
git checkout -b develop
git push -u origin develop
# create feature branch
git checkout -b feature/logo-anim
name: CI
on:
  push:
    branches: [ main, develop ]
  pull_request:
    branches: [ main, develop ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Set up Node
        uses: actions/setup-node@v4
        with:
          node-version: '18'
      - name: Install
        run: npm ci || true
      - name: Run tests (if any)
        run: npm test || echo "no tests"
# install pre-commit (local)
pip install pre-commit
cat > .pre-commit-config.yaml <<'EOF'
repos:
- repo: https://github.com/pre-commit/mirrors-prettier
  rev: '' # choose version
  hooks:
    - id: prettier
EOF

pre-commit install
Primary logo: logo.svg (use on light backgrounds)
Alternate: logo-white.svg (use on dark)
Animation: logo-anim.json (Lottie or export to mp4/gif for reels)
# scripts/ai-news/summarize.py
# NOTE: fetch only from permitted public RSS/feeds and respect robots.txt and TOS
import feedparser
from datetime import datetime

FEEDS = ["https://example.com/rss"]

def fetch_and_summarize():
    for feed in FEEDS:
        d = feedparser.parse(feed)
        for entry in d.entries[:5]:
            title = entry.title
            link = entry.link
            published = entry.get("published", "")
            # Save a markdown note in content/ai-news/
            with open(f"content/ai-news/{datetime.utcnow().isoformat()}-{title[:50]}.md", "w") as f:
                f.write(f"# {title}\n\n{link}\n\nPublished: {published}\n\nSummary: (manual)")
---
name: Content idea
about: Propose a new post/reel
---

**Title / Hook**:
**Type**: [Reel | Carousel | Caption]
**Script / Caption**:
**Assets**:
**Publish date (UTC)**:
**Notes**:
git fetch origin
git pull origin main
git revert <commit-hash>
# or for last commit not pushed
git reset --soft HEAD~1
# create branch
git checkout -b feature/my-feature

# stage & commit
git add .
git commit -m "message"

# push
git push origin feature/my-feature

# create PR via gh (GitHub CLI)
gh pr create --base develop --head YOUR_USER:feature/my-feature --title "Title" --body "Description"
mkdir neural-ghost && cd neural-ghost
git init
git branch -m main
echo "# Neural Ghost" > README.md
echo "node_modules/" > .gitignore
mkdir -p branding/logo content/instagram content/reels scripts/ai-news website/public
git add .
git commit -m "Initial Neural Ghost repo structure"
git remote add origin git@github.com:YOUR_USER/neural-ghost.git
git push -u origin main

