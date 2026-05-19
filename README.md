# Vestigia

> *From the Latin — footprints, traces, marks left behind.*
> *The evidence that something passed this way.*

---

**Vestigia** is an open framework for final-year students documenting, making sense of, and presenting their capstone project work.

It is not a log book template. It does not tell you what to write or how often.

It builds the habit and the thinking behind a genuine project record — one that is honest enough to be useful during the project, and specific enough to be professionally valuable after it ends.

---

## The Live Guide

The full Vestigia guide is published at:

**[jesselsookha.github.io/Vestigia](https://jesselsookha.github.io/Vestigia/)**

Read it there. It is structured for navigation, not for browsing raw files.

---

## The Philosophy Behind Vestigia

Most final-year students finish their project and find themselves unable to explain it properly.

Not because the work was poor. Because the thinking disappeared.

The decision to choose one framework over another, the three days spent on a problem that turned out to be a wrong assumption, the meeting where the client said something that changed the entire direction — none of it was recorded. By the time reports were written and reflections submitted, it had been reconstructed from memory into something tidier, safer, and less true.

Vestigia is built on a different premise:

> *A brief, honest entry written at the moment of a decision is worth more*
> *than a paragraph reconstructed three months later.*
> *The record is not overhead. It is the work.*

The tradition behind this is long. The engineering log book, the lab notebook, the project diary — professional and academic practice has always known that the record of how work happened is as important as the work itself. What has broken down is the fit between that tradition and how contemporary students actually work: digitally, collaboratively, across tools, and under time pressure.

Vestigia updates the tradition without abandoning it. The habit stays. The friction goes.

---

## What Vestigia Covers

| Section | Focus |
|---------|-------|
| Guide A | Recording the project as a living process — five categories of meaningful entry, when to write, what format to use, and why the early weeks matter most |
| Guide B | Turning records into professional evidence — extraction filters, narrative construction, integrity in presenting collaborative work, and the connection to wider portfolio development |
| Shared Presence | Building a collective group presence that communicates the project to external audiences — project websites, platform options across disciplines, and what makes a group site worth visiting |
| For Lecturers | A full orientation for supervisors and module coordinators — what the framework is, how it works in practice, how to mention it to students, and how it connects to existing assessment structures |

---

## Who This Is For

Vestigia is written for:

- final-year undergraduate students in any discipline, at the start of or during their capstone project
- students approaching the end of a project who need to present their work professionally
- groups building a collective presence for a shared project
- lecturers, supervisors, and module coordinators who want to understand or introduce the framework

It is written primarily with Computer Science, IT, and Engineering students in mind — disciplines where the log book tradition is most deeply rooted, and where Agile methodology, client projects, and full-stack development create the most immediate need for intentional record-keeping.

The framework is discipline-agnostic in practice. If your project involves decisions, iteration, and learning over time — Guide A applies to you.

---

## The Connection to Itan

Vestigia is a companion project to **[Itan](https://jesselsookha.github.io/Itan/)** — an open portfolio development framework for students and professionals across all disciplines.

Where Vestigia focuses on *one project, documented while it happens*, Itan addresses the broader question: *how do I build and maintain a professional portfolio across my entire career?*

The two projects are independent — either can be used without the other — but they are designed to work together. Vestigia records produce the most specific, honest, and richly documented portfolio material a student is likely to have at the point of graduation. Itan shows how to place that material within a wider professional narrative.

Guide B of Vestigia connects directly to Itan. Students who complete their capstone showcase through Guide B have the foundation for everything Itan builds on top of it.

---

## Repository Structure

```
vestigia/
├── docs/
│   ├── index.md                          # Home page
│   ├── guide-a/                          # During the project
│   │   ├── index.md
│   │   ├── 01-foundations.md
│   │   ├── 02-guide.md
│   │   └── 03-examples.md
│   ├── guide-b/                          # After the project
│   │   ├── index.md
│   │   ├── 01-foundations.md
│   │   ├── 02-guide.md
│   │   ├── 03-extraction-prompts.md
│   │   ├── 04-from-fragments-to-showcase.md
│   │   └── 05-integrity-and-attribution.md
│   ├── shared-presence/                  # Optional collective layer
│   │   ├── index.md
│   │   ├── 01-what-is-a-shared-presence.md
│   │   ├── 02-project-website.md
│   │   └── 03-other-disciplines.md
│   ├── for-lecturers/                    # Staff orientation
│   │   ├── index.md
│   │   ├── 01-what-vestigia-is.md
│   │   ├── 02-how-it-works.md
│   │   ├── 03-mentioning-it-to-students.md
│   │   └── 04-assessment-and-integration.md
│   └── stylesheets/
│       └── extra.css
├── mkdocs.yml
├── requirements.txt
└── .github/
    └── workflows/
        └── deploy.yml
```

---

## Running Locally

```bash
pip install -r requirements.txt
mkdocs serve
```

The site will be available at `http://127.0.0.1:8000`. Changes to any file rebuild the site automatically.

---

## Using and Adapting This Work

Vestigia is open. If something here is useful to your students, your department, or your institution — use it, adapt it, share it.

If you find gaps, have suggestions, or want to discuss the ideas behind it, contributions and conversations are welcome.

---

## About the Author

Vestigia was developed by **Jessel Sookha**, a lecturer in Information Technology with a long-standing interest in how students document, reflect on, and present the work they produce during their studies.

It grew from the same nine years of thinking that produced Itan — from the persistent observation that students who do good work often cannot explain it, and that this gap is not a communication problem. It is a documentation problem. And documentation problems have solutions.

- GitHub: [github.com/jesselsookha](https://github.com/jesselsookha)
- LinkedIn: [linkedin.com/in/jesselsookha](https://www.linkedin.com/in/jesselsookha/)
- Itan: [jesselsookha.github.io/Itan](https://jesselsookha.github.io/Itan/)

---

*The record is not overhead. It is the work.*