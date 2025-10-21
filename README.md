# Ethical Hacking Journal — Sam (Full Learning Journey)

**A living, public learning log documenting my ethical hacking journey — from Linux fundamentals to advanced red-teaming.**  
This repository is my single source of truth for everything I learn, build, test, and teach about offensive security and defensive thinking. It contains reproducible scripts, day-by-day notes, challenge write-ups, sanitized captures, projects, and certification prep — all produced in legal, controlled labs.

---

## Badges
> Replace the placeholders below with your actual account IDs/handles.

[![TryHackMe: smmburu](https://img.shields.io/badge/TryHackMe-smmburu-yellow)](https://tryhackme.com/p/smmburu)
[![WakaTime](https://wakatime.com/badge/user/.svg)](https://wakatime.com)  
[![GitHub stars](https://img.shields.io/github/stars/smmburu/ethical-hacking-journal)](https://github.com/smmburu/ethical-hacking-journal/stargazers)

## 🕒 WakaTime Stats
<!--START_SECTION:waka-->
<!--END_SECTION:waka-->

## 🧠 TryHackMe Progress
![TryHackMe Stats](https://github.com/smmburu/ethical-hacking-journal/blob/main/metrics.svg)

---

## Table of contents
- [What this repo is](#what-this-repo-is)  
- [Why I keep a public journal](#why-i-keep-a-public-journal)  
- [Core principles & rules](#core-principles--rules)  
- [Repo structure](#repo-structure)  
- [Phases & roadmap (overview)](#phases--roadmap-overview)  
- [How I work — workflow & templates](#how-i-work---workflow--templates)  
- [Setup & quick start (clone + run)](#setup--quick-start-clone--run)  
- [How to contribute / collaborate](#how-to-contribute--collaborate)  
- [License & attribution](#license--attribution)  
- [Contact & social proof](#contact--social-proof)

---

## What this repo is
`ethical-hacking-journal` is a chronological, technical, and verifiable record of my cybersecurity learning. It’s intentionally practical — not polished marketing. Each deliverable shows *what I actually did* (commands, scripts, outputs, sanitized artifacts) and *what I learned*. Over time the repo will grow from beginner content into intermediate and advanced projects.

---

## Why I keep a public journal
- **Accountability:** daily/weekly logs force regular practice.  
- **Evidence:** real outputs (scripts, writeups, PCAPs) show skill growth far better than claims.  
- **Shareability:** peers and recruiters can follow progress and give feedback.  
- **Teaching:** explaining solutions solidifies my understanding and helps others.

---

## Core principles & rules I follow
1. **Legal & ethical only.** I only test machines in lab environments or on targets where I have explicit permission.  
2. **Reproducible.** Scripts and write-ups include environment notes, exact commands, and expected outputs.  
3. **Sanitized artifacts.** No real credentials or private data in commits. PCAPs and logs are sanitized.  
4. **Incremental commits.** Small, frequent commits with meaningful messages.  
5. **Transparency.** Dates, context, and problem statements are included on each write-up.

---

## Repo structure
```
ethical-hacking-journal/
├── scripts/                # reusable scripts (bash, python, powershell)
│   ├── sysinfo.sh
│   └── netscan.sh
├── notes/                  # daily notes and weekly summaries (markdown)
│   ├── day-001-wsl-setup.md
│   ├── day-002-commands.md
│   └── week-01-summary.md
├── writeups/               # CTF/room/machine writeups
│   ├── bandit-00.md
│   ├── tryhackme-room-name.md
│   └── htb-box-name.md
├── resources/              # cheatsheets, links, static html navigator, assets
│   └── ethical-hacking-resources.html
├── pcaps/                  # (sanitized) captures for analysis
├── projects/               # larger projects (tools, automation, research)
├── ROADMAP.md              # detailed roadmap beginner→advanced
├── .gitignore
├── LICENSE
└── README.md
```

---

## Phases & roadmap (overview)
This is a living roadmap — the contents below will evolve as I learn.

- **Phase 0 — Setup (Day 0)**  
  WSL / Linux install, VS Code + Remote WSL, initial tooling (`git`, `nmap`, `tcpdump`, `python3`, `vim`).

- **Phase 1 — Foundations (21 days)**  
  Linux & CLI mastery, basic shell scripting, OverTheWire Bandit, sysadmin basics.

- **Phase 2 — Networking & Enumeration (Weeks 4–6)**  
  TCP/IP, `nmap` scanning, `tcpdump`/Wireshark, netcat, basic service enumeration.

- **Phase 3 — Web & Application Security (Weeks 7–9)**  
  HTTP, OWASP Top 10, Juice Shop, Burp Suite basics, SQLi/XSS exploration in labs.

- **Phase 4 — Host Exploitation & Privilege Escalation (Weeks 10–13)**  
  Enumeration, common LPE vectors, linpeas/winpeas, sudo misconfigurations, kernel vectors.

- **Phase 5 — Post-exploitation, Persistence & Lateral Movement**  
  Credential harvesting, pivoting, persistence, and detection/defense tradeoffs.

- **Phase 6 — Advanced Topics & Research**  
  Reverse engineering, memory forensics, fuzzing, exploit development, red teaming.

- **Certifications & projects**  
  Track study notes for eJPT → OSCP → advanced certs. Build reproducible tools, papers, and demos.

(See `ROADMAP.md` for a week-by-week plan and specific deliverables.)

---

## How I work — workflow & templates
A repeatable daily workflow keeps the journal consistent and useful.

1. **Do the work** in WSL / local lab.  
2. **Log the results** immediately in `notes/day-XXX-*.md` with command history and short commentary.  
3. **Create/update writeups** for any challenge completed in `writeups/`. Include goal, environment, commands, sanitized output, and lessons learned.  
4. **Commit & push** with clear messages:
```bash
git add .
git commit -m "day-014: finished Bandit lvl 7 — used find/grep; added writeup"
git push
```

### Daily note template (`notes/day-###-title.md`)
```markdown
# Day ### — Short Title
**Date:** YYYY-MM-DD  
**Sprint / Phase:** Phase 1 — Linux & CLI

## Goal
(one line: what I wanted to accomplish)

## Environment
- Distro: Ubuntu 24.04 on WSL2
- Host: Windows 11
- Tools: bash, nmap, python3, vim

## Commands run
```
# paste exact commands you ran
sudo apt update && sudo apt install nmap -y
nmap -sC -sV 10.0.2.15 -oN scan.txt
```

## Findings / Output (sanitized)
- Key results, shortened output, or link to `pcaps/` or artifact.

## Problems & Fixes
- What broke and how it was fixed.

## Lessons learned
- Short bullets

## Next
- Plan for tomorrow.
```

### Writeup template (`writeups/name.md`)
```markdown
# Writeup: [Name / Room / Box]
**Date:** YYYY-MM-DD  
**Difficulty:** Beginner / Intermediate / Advanced  
**Target:** IP / Room / VM (lab only)

## Objective
- What the challenge asks.

## Enumeration
- Commands used to enumerate and what they revealed.

## Exploitation
- Exact commands or steps to exploit (sanitized).

## Privilege Escalation
- Steps and reasoning.

## Post-exploitation & cleanup
- What was explored and how the environment was left.

## Lessons
- What to improve, references, mitigation ideas.
```

---

## Setup & quick start (clone + run)
```bash
# clone repo
git clone https://github.com//ethical-hacking-journal.git
cd ethical-hacking-journal

# run system summary (example)
bash scripts/sysinfo.sh
```
**Note:** Replace `` with your GitHub handle.

---

## Recommended initial scripts
- `scripts/sysinfo.sh` — quick environment snapshot (hostname, uptime, memory, disks, top processes, network interfaces).  
- `scripts/netscan.sh` — templated `nmap` scans and output formatting.  
- `scripts/backup.sh` — quick backup of notes and writeups before major changes.

---

## How to contribute / collaborate
I welcome:
- Corrections to techniques and scripts.  
- PRs that add better examples or improve documentation.  
- Suggestions for new learning resources or challenge writeups.

**Before you open a PR:**
- Keep changes focused and documented.  
- Don’t add secrets or raw credentials.  
- Include tests or sample runs if you add a new script.

---

## License & attribution
This repository is licensed under the **MIT License**. See the `LICENSE` file for details.  
You are free to reuse and adapt the educational scripts and notes — please attribute and follow the rules in the license.

---

## Contact & social proof
- **Owner:** Sam — Nairobi, Kenya  
- **LinkedIn:** https://linkedin.com/in/isammburu
- **TryHackMe:** https://tryhackme.com/p/smmburu

---

## Final notes
This repo is intentionally public and iterative. Expect rough drafts, typos, and experimental code — that’s the point: it’s a real record of learning by doing. If you want, I can now generate `ROADMAP.md`, populate `notes/day-001-wsl-setup.md`, or create the initial scripts (`sysinfo.sh`, `netscan.sh`) ready to paste into the `scripts/` folder.
