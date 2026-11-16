<div align="center">

# PMM Skills for Claude

**Two Claude skills for product marketing teams: one runs a launch, one keeps competitive research current.**

![Claude Skills](https://img.shields.io/badge/Claude-Skills-111111?style=flat-square)
![Skills](https://img.shields.io/badge/skills-2-111111?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-111111?style=flat-square)

[What's inside](#whats-inside) · [Install](#install) · [Set up](#set-up) · [Use](#use) · [Make them yours](#make-them-yours)

</div>

---

## Why these exist

Most launch and competitive work repeats. The same brief turns into the same set of assets, and the same competitors get checked every week. These two skills hold that routine so a product marketer can spend time on judgment: what the story is, what to leave out, and what a competitor's move means.

Both skills produce drafts for a person to edit. Neither sends, posts, or publishes anything.

## What's inside

| Skill | What it does | You give it | You get back |
| --- | --- | --- | --- |
| **[Launch Manager](launch-manager/)** | Plans and drafts a product or feature launch | A release transcript or product notes | An internal brief, a launch plan, a blog draft, emails, social posts, a sales brief, and announcements |
| **[Competitive Research Manager](competitive-research-manager/)** | Tracks competitors and turns findings into material sales can use | Your competitor list, by tier | A change-only weekly report, battlecards, and focused comparisons |

<details>
<summary><b>Launch Manager in detail</b></summary>

<br>

Works through a six-step launch motion. Use all six or jump to one.

| Step | Output |
| --- | --- |
| 1. Release synthesis | The internal brief every other asset is built from |
| 2. Launch plan | A checklist across pre-launch, launch week, and post-launch |
| 3. Launch blog | A full draft with headline options |
| 4. Customer session | Agenda, talking points, follow-up |
| 5. Market-facing webinar | Abstract, outline, promotion emails |
| 6. Strategic evaluation | Goal, measures, risks |

It also sizes the launch into one of three tiers, so a small release does not get a large launch.

Rules it holds to:

- Only shipped capability is described as available
- No invented numbers, customers, or quotes
- One call to action per asset
- A check on every asset before it is handed over

</details>

<details>
<summary><b>Competitive Research Manager in detail</b></summary>

<br>

Does three jobs.

| Job | When to use it |
| --- | --- |
| Weekly change report | On a schedule. Reports only what changed and passed a materiality test. |
| Battlecard | For a new competitor, or a card older than 90 days |
| Competitive brief | Before a launch, a deal, or a positioning decision |

Rules it holds to:

- Every claim links to a page it opened
- Facts and inferences are labeled separately
- Each competitor gets an honest "where they are better"
- Risk levels change only when a named trigger fires
- Public sources only

</details>

## Repository layout

```
.
├── launch-manager/
│   ├── SKILL.md
│   └── references/
│       ├── company-context.md      <- fill this in first
│       ├── launch-steps.md
│       ├── asset-templates.md
│       └── launch-log.md
├── competitive-research-manager/
│   ├── SKILL.md
│   └── references/
│       ├── company-context.md      <- fill this in first
│       ├── battlecard-template.md
│       └── report-format.md
├── dist/
│   ├── launch-manager.zip
│   └── competitive-research-manager.zip
├── LICENSE
└── README.md
```

## Install

### Claude (web and desktop apps)

1. Download the ZIP for the skill you want from [`dist/`](dist/).
2. In Claude, go to **Customize > Skills**.
3. Click **+**, then **Create skill**, then **Upload a skill**.
4. Upload the ZIP.

Skills need code execution and file creation turned on. On Team and Enterprise plans an owner may need to enable skills for the organization first. Menus can change, so see [Anthropic's guide to custom skills](https://support.claude.com/en/articles/12512180) if these steps do not match what you see.

### Claude Code

Copy the skill folder into your personal skills directory:

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git
cp -r YOUR-REPO/launch-manager ~/.claude/skills/
cp -r YOUR-REPO/competitive-research-manager ~/.claude/skills/
```

## Set up

Each skill ships with a `references/company-context.md` file full of placeholders. Fill it in before the first real run. Until you do, the skill will ask for the missing details.

| Skill | What to fill in |
| --- | --- |
| Launch Manager | Positioning statement, pillars, personas, vocabulary, voice rules, proof you can cite, channels and owners |
| Competitive Research Manager | Your own positioning, competitors by tier, watch sources for each, and the triggers that would change a risk level |

Keep it short. One page that is true is worth more than five that are out of date.

## Use

Once installed, ask in plain language. Claude picks up the skill from the request.

**Launch Manager**

```
Here is the transcript from our product call. Plan the launch.
```
```
Draft the launch blog and three social posts for this release.
```
```
Build a sales brief for the feature we ship next week.
```

**Competitive Research Manager**

```
Run the weekly competitive update.
```
```
Build a battlecard for [competitor].
```
```
We are launching [feature]. How does it compare to what [competitor] offers?
```

## Make them yours

These are starting points. They get better the more your own corrections go back into them.

- **After each launch**, the Launch Manager asks what you had to correct. Record the answer in `launch-log.md`, or in `company-context.md` if it applies to every launch.
- **When a competitor changes**, the research skill updates the existing record and adds a dated line to its change log.
- **Edit freely.** Each skill is a folder of Markdown files. Change the steps, the templates, or the rules to match how your team works.

## A note on how to use the output

A skill is fast and consistent. It does not know your customers, and it cannot tell which claim your legal team will reject. Read every draft before it goes anywhere, check each number against its source, and treat the output as a first draft from a capable colleague.

## Author

Built by [Lucio Daza](https://github.com/YOUR-USERNAME), from the way I run launches and competitive research as a product marketer. Shared freely. If you improve one, a pull request is welcome.

## License

[MIT](LICENSE)
