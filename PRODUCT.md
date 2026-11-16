# Product

<!-- impeccable:product-schema 1 -->

> Revised on 2026-11-16 from the owner's own feedback on the first proposal, Saltech's internal positioning notes (kept outside this repository), the 2021 site and the Lockey You project files.
> Lines marked *(hypothèse)* are still unconfirmed. On the site, `hypotheses: true` shows stamps on every unconfirmed fact.

## Platform

web

## Users

- Primary: a public buyer, IT director, prime contractor or recruiter who types "Jean-Paul Tossou" before working with him or with Saltech. Buyers verify more than they discover. They arrive from a search, LinkedIn or a bid file, usually on a work laptop. Within thirty seconds they need: role and seniority, the three trades, where he has worked, how to engage (Saltech for a team, direct contact otherwise).
- Secondary: CTOs and engineers judging technical depth (the Lockey You case study, the notes), and developers landing on a note from a search.

## Product Purpose

The reference page of the founder of Saltech: proves seniority and depth, sends team work to Saltech, and hosts signed technical notes. Replaces the unfinished 2021 site and the first proposal of 2026-11-16, which the owner judged too superficial ("ça pourrait supposer que je suis un débutant") and silent on what he does.

## Positioning

"Fondateur de Saltech, architecte logiciel": the same words on every founder profile (LinkedIn, GitHub, this site). One architect across three trades usually held by separate specialists:

1. Business software and mobile apps. Native Android and iOS since 2015 (Java, Kotlin, Swift), Flutter when one codebase must serve both. Certified Java and Kotlin *(hypothèse: exact certifications)*. Since 2022 for a homeland-security actor. Also the European Commission's IT directorate (DIGIT) and retail (Carrefour, Carrefour Assurance) *(hypothèse: periods and work)*. Independent since 2020; Saltech since 2024.
2. Data engineering, still practised. Pipelines, ETL, warehouses, data quality, observability. Two years for a multi-site aerospace manufacturer, then a construction company and an insurer *(hypothèse: dates)*. Master's degree "Industrie 4.0" (data science, data engineering), Université de Pau et des Pays de l'Adour.
3. Connected objects and home automation, his field of choice. Co-founder and CTO of Lockey You, built with a team (never "I built it alone") *(hypothèse: title)*; connected scent diffuser (2020 to 2021).

Missions and responsibility come first; technology lists stay short and last.

## Operating Context

- Hosting: GitHub Pages, "deploy from a branch" on `master` of `cresusjpt/cresusjpt.github.io`, custom domain `www.jeanpaultossou.tech`. No server: a firm owner constraint.
- Publishing a note = one Markdown file in `_posts/` + `git push`.
- Contact: e-mail first (jeanpaul.tossou@saltech.fr). A form appears only if `contact_form` holds a working third-party endpoint; the 2021 getform.io address now redirects to Forminit's home page and was removed.

## Capabilities and Constraints

- Jekyll 3.10 through the `github-pages` gem; only whitelisted plugins (jekyll-feed, jekyll-seo-tag, jekyll-sitemap).
- Language: French.
- Writing rules shared with Saltech: no em dash in site copy, no hollow jargon, never invent a fact (client reference, figure, certification, headcount).
- Reference policy: name the entity or the sector with the work actually done; no contractual frame on the site (owner's decision, 2026-11-16); never call an entity served through an intermediary a "client"; no logos; no project details. Homeland security stays at sector level ("un acteur de la sécurité intérieure") until a written agreement allows naming.
- Trajectory: "since 2020" belongs to the founder's activity; Saltech was created in 2024.
- Lockey You: never publish supplier names, costs or customer names.
- The apex domain `jeanpaultossou.tech` does not point to GitHub Pages yet (DNS fix on the owner's side; Google Workspace MX records stay untouched).

## Brand Commitments

Visual world: the technical drawing sheet recorded in DESIGN.md. The owner approved it ("j'aime bien le truc") and asked for depth, not a new look. Name spelled "Jean-Paul Tossou".

## Evidence on Hand

- Owner's statements of 2026-11-16 (degrees, years, trades, references, Saltech, Lockey You).
- Saltech's internal positioning notes: team wording ("une équipe et un réseau de consultants seniors"), founder title, reference policy.
- Lockey You repository and docs: architecture, 69 ADRs, about 9,300 tests, KiCad board, first web platform in December 2023, in service since June 2024, production status (as of 2026-11-12). Deliberately left off the site: commit count.
- 2021 site: Google mentor for mobile development, certifications listed on LinkedIn.
- Public GitHub repositories: DWWM and CDA training material (trainer, 2022 to 2023 *(hypothèse: dates)*).
- Portrait of 2026 supplied by the owner. No testimonial, no client figure, no published article yet.

## Product Principles

1. Thirty seconds to know who, what, where and how to engage.
2. Prove with missions, roles and products; adjectives and technology lists stay secondary.
3. The same facts as saltech.fr and LinkedIn.
4. Publishing stays one Markdown file and a push.
5. No server, no tracker, fast everywhere.

## Accessibility & Inclusion

WCAG 2.2 AA: contrast in both themes, keyboard navigation, labelled form fields, tables readable when stacked on phones, reduced motion respected.
