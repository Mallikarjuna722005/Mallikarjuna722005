# GitHub Profile Redesign: Audit, Setup and Publishing Guide

Target profile: https://github.com/Mallikarjuna722005
Candidate: Mallikarjunaswamy C

Files delivered (all in one flat folder):

| File | Goes to | Purpose |
| --- | --- | --- |
| `README.md` | repo root | The new profile README |
| `header.svg` | repo root (same folder as README) | Self-hosted banner, no third-party service |
| `snake.yml` | `.github/workflows/snake.yml` | Corrected contribution-snake workflow |

Nothing was pushed to GitHub. All publishing is done by the account owner using the steps in section E.

---

## Identity resolution

| Source | Name / username | Verdict |
| --- | --- | --- |
| Resume `Malli.pdf` | Mallikarjunaswamy C | Candidate |
| Live profile page | Display name "Mallikarjunaswamy C", user `Mallikarjuna722005` | Same person |
| Live profile README | Same name; same LinkedIn; email `mallikarjunaswamy.c112005@gmail.com` | Matches the resume email prefix |
| Commits in `APP` | Author "Mallikarjunaswamy C" | Confirms ownership |
| ZIP `anandd46-main.zip` | Anand D, `anandd46` | Different person |

Result: the ZIP is another person's profile. Its name, email, LinkedIn, LeetCode, HackerRank, portfolio, certifications, hackathon claim and project list were **not** copied. Only its layout ideas and snake workflow were reused as a starting point.

The resume prints the email as `@email.com`, which looks like a PDF conversion artefact. The README uses the `@gmail.com` address shown on his own live GitHub README.

---

## A. Profile audit

### A1. The ZIP README (Anand D)

**Strengths:** consistent dark-navy and cyan palette, light/dark snake `<picture>` pattern, clear section order.

**Problems**
- Wrong identity throughout (name, username, email, LinkedIn, LeetCode, HackerRank, portfolio).
- Eight role titles in the banner and typing animation, plus an "Open to Work" block for eight roles.
- Unsupported claims for this candidate: Smart India Hackathon 2024, "production-grade" deployed AI projects, AWS VPC and CI/CD work, seven certifications from issuers not on the resume.
- Language levels contradict the resume (Tamil listed as Native; resume says limited working proficiency).
- Roughly 40 technology icons (Java, C#, PHP, React, Kubernetes, LangChain, AWS, and more) that do not appear on the resume.
- Six projects, none verifiable under the target account.
- Reliability: the stats, streak, trophy, activity-graph and quote widgets are all separate third-party services. The Heroku-hosted streak card in particular is a common failure point.
- The snake section is a "how to set it up" note left in the published README.
- Decorative extras: typing animation, view counter, quote card, double footers, duplicated `---` rules.

### A2. The existing live README for `Mallikarjuna722005`

**Strengths:** correct identity and contact links, short and mostly honest project list.

**Problems**
- The "Snake" section only shows the text `.github/workflows/snake.yml`. The profile repo contains **only** `README.md`, so no snake workflow exists.
- Heading "AI / ML Expertise" with entries like "Model Development" overstates a student-level skill set and says nothing specific.
- The tech icon row includes Java, MySQL, Linux and VS Code, which the resume does not list (the resume lists SQL, not MySQL). Java is also named as the AgroSmart language, but the resume does not say that.
- "Academic IoT communication prototype" for the Wireless Transmission Model: the resume says wireless data transmission, not IoT.
- Four stat and trophy widgets from separate third-party hosts, with no alt text.
- No links from projects to repositories; the project descriptions are one line each.
- Banner, typing animation and footer all depend on external services.

### A3. Changes made in the new README

- One truthful tagline instead of a list of roles; no "open to every job" badges.
- Every skill sits next to evidence ("Where it shows up").
- Only two projects are featured, because only two repositories exist, and each states its actual status.
- Resume-only projects are listed separately and labelled as not yet on GitHub.
- Banner is a local `header.svg`; the README stays readable if every external image fails (all images have alt text, and the headline and tagline are real text).
- Light/dark variants for the snake and stats card.
- CGPA, school marks and phone number are intentionally left out of the public page.

---

## B. Repository audit

Public repositories seen on the account: **3** (checked by cloning each one).

| Repository | Contents (verified) | Last commit | Use in README |
| --- | --- | --- | --- |
| `Research` | `README.md` (just a title) and `Cucumber Architecture`, a text architecture document for cucumber growth-stage detection: smartphone image capture, 224×224 resize and augmentation, EfficientNetV2 / ResNet50 / VGG16 feature extraction, softmax head over five stages, evaluation metrics, and a deployment outline | 2025-04-24 | **Featured** as Cucumber Growth Stage Detection, labelled "architecture documented; notebooks and results not yet published" |
| `APP` | Five Jupyter notebooks: exception handling (two), functions and lambda, pattern problems (59 cells), and scenario case studies | 2026-09-10 | **Featured** as Python Practice Notebooks |
| `Mallikarjuna722005` | Profile README only | 2026-07-13 | Replaced by the new README |

**Projects in the old READMEs that could not be verified**

| Claim | Where it appeared | Handling |
| --- | --- | --- |
| AgroSmart (Java application) | Live README | Shown with the resume's wording only, no language claimed, no link |
| Wireless Transmission Model (IoT prototype) | Live README | Shown with the resume's wording only |
| AI Chatbot, CodeSage AI, House Price Prediction, Web Expense Tracker, AWS VPC, CI/CD Pipeline, Smart Agriculture AI | ZIP README (Anand D) | Omitted entirely; no matching repositories |

**Could not be verified**
- Whether private repositories exist (invisible to anyone else).
- The cucumber model's accuracy or any training results (none published).
- Deployed demos (none found).
- The LinkedIn URL being live (copied from his own live README).

---

## C. Final README: what to confirm before publishing

1. **Email**: `mallikarjunaswamy.c112005@gmail.com` is taken from his live README. Confirm it is the one he wants public.
2. **"Current Focus"** (full-stack, advanced ML, MLOps, cloud) comes from the Current Focus block of his existing README. Edit if outdated.
3. **Certifications** are the exact resume titles with no issuer, ID or link, because none are supported by evidence. Add the issuer and credential link for each when available.
4. **Open to** line: "software development and AI/ML internship opportunities" is based on his existing README ("Software Engineering", "AI/ML Internships") and the resume summary. Adjust if he wants something different.
5. **Java**: not listed as a skill because the resume does not list it. If he has Java project work, add it, ideally with a repository.

**Strengthening the profile (recommended, takes the most effect)**
- Upload the cucumber-detection notebooks, a short results table and a few sample predictions to `Research`, then update the status line in the README. Report only real numbers.
- Upload AgroSmart and the Wireless Transmission Model with a short README each, then link them.
- Rename `APP` to something descriptive such as `python-practice-notebooks` (GitHub redirects the old URL, but update the two links in the README after renaming).
- Pin the two featured repositories on the profile and add a one-line description and topics to each.

---

## D. Snake workflow (`snake.yml`)

**What changed from the ZIP version**

| Item | ZIP version | New version | Why |
| --- | --- | --- | --- |
| Snake action | `Platane/snk@v3` | `Platane/snk/svg-only@v3` | Faster; SVG output only, which is all the README uses |
| Pages action | `crazy-max/ghaction-github-pages@v3` | `@v5` | v3 is outdated; v5 runs on current Node |
| Checkout step | `actions/checkout@v3` | Removed | Not needed; one fewer dependency |
| Schedule | Every 6 hours | Daily | The contribution graph changes at most daily |
| Extras | none | `concurrency`, `timeout-minutes` | Prevents overlapping or hung runs |

The action versions were checked against the upstream repositories: `Platane/snk` v3 series, `crazy-max/ghaction-github-pages` v5. The workflow file was parsed as valid YAML locally. It has not been run on GitHub, since that requires the owner's repository.

**Setup (one-time)**
1. Create the folder path `.github/workflows/` in the profile repository and save `snake.yml` there.
2. In the repository go to **Settings → Actions → General → Workflow permissions** and select **Read and write permissions**, then Save.
3. Go to the **Actions** tab, choose **Generate Snake**, click **Run workflow**.
4. When it finishes, confirm a branch named `output` exists and contains `github-snake.svg` and `github-snake-dark.svg`.
5. After that it runs daily. If the repository is idle for a long time GitHub may pause scheduled workflows; re-enable from the Actions tab or run it manually.

No secrets are needed: `GITHUB_TOKEN` is provided automatically by GitHub Actions.

---

## E. Installation and publishing steps

Run these on the account owner's machine.

**1. Confirm the correct repository**
A profile README only works from a **public** repository whose name equals the username exactly: `Mallikarjuna722005/Mallikarjuna722005`. It already exists, and its `README.md` is the one shown on the profile page. Check in the browser that the repo name matches before you replace anything.

**2. Clone and back up**
```bash
git clone https://github.com/Mallikarjuna722005/Mallikarjuna722005.git
cd Mallikarjuna722005
cp README.md README.backup.md        # local backup (do not commit this file)
git checkout -b profile-redesign     # work on a branch, not main
```

**3. Add the new files** (adjust the source path to where you saved the downloads)
```bash
cp /path/to/downloads/README.md .
cp /path/to/downloads/header.svg .
mkdir -p .github/workflows
cp /path/to/downloads/snake.yml .github/workflows/snake.yml
```

**4. Review**
```bash
git status
git diff --stat
```
Only `README.md` should be modified, and `header.svg` and `.github/workflows/snake.yml` should be new. Read the README once and confirm the items in section C. Do not commit `README.backup.md`; delete it or add it to `.git/info/exclude`.

**5. Preview**
- Open `README.md` in VS Code and press `Ctrl+Shift+V` (Markdown preview), or
- Push the branch (step 6) and open the file on the branch in GitHub, which renders it exactly as the profile will.

Images from shields.io and the stats card load only when online.

**6. Commit and push**
```bash
git add README.md header.svg .github/workflows/snake.yml
git commit -m "Redesign profile README; add snake workflow"
git push -u origin profile-redesign
```
Open the pull request or merge to `main` once the preview looks right:
```bash
git checkout main
git merge profile-redesign
git push origin main
```

**7. Run the snake workflow** (section D, steps 2 to 4). The snake image will show its alt text until the first run finishes.

**8. Verify after publishing**
- Open https://github.com/Mallikarjuna722005 in a normal window and a private window.
- Switch GitHub between light and dark theme (Settings → Appearance) and check the banner, snake and stats card in both.
- Click every link: both repositories, LinkedIn, GitHub, email.
- Check the Actions tab for a green run.
- View on a phone-width window; the tables should scroll or wrap without breaking the page.

---

## F. Final quality checklist

| Area | Check | Status |
| --- | --- | --- |
| Identity | Name, username, LinkedIn, email belong to the target; no ZIP personal data present | Pass (searched for leaked terms) |
| Accuracy | Education, skills, projects, certifications and languages match the resume; project details match repository contents | Pass |
| Claims | No metrics, awards, deployments, issuers or credential IDs invented; unverified items labelled | Pass |
| Repository ownership | All links point to `Mallikarjuna722005`; both repos exist (cloned) | Pass |
| Markdown | Rendered with cmark-gfm (GitHub's parser); no unclosed or mismatched HTML tags; table columns consistent | Pass |
| Rendering of HTML cells | Headings and lists render inside the project table | Pass |
| Accessibility | Every image has descriptive alt text; heading levels `##`/`###` consistent; banner SVG has title and description | Pass |
| Failure behaviour | Header text, tagline and skills remain readable if all external images fail | Pass by design |
| Widgets | Snake is self-hosted via Actions; stats card is third-party and best-effort | **Not verified live**: the test environment cannot reach shields.io or Vercel hosts. Check after publishing |
| Workflow | YAML parses; action versions match upstream tags | Pass locally; first real run pending |
| Privacy | No phone number, CGPA or school marks, tokens or secrets | Pass |

**Known limitations**
- The GitHub stats card (`github-readme-stats.vercel.app`) is a public instance that can rate-limit or go down. With 3 repositories and 1 follower the numbers will be small. If it looks empty or fails, delete that `<picture>` block; nothing else depends on it.
- A top-languages card was deliberately not included: with only notebooks it would report "Jupyter Notebook" and say nothing about skill.
- The snake does not appear until the workflow has run once.
