# 00. Integration Guide: From Bibliography to Research Ecosystem

## Purpose

This file describes how to integrate the expansion files into the existing `biblical-scholarship` repository. The current repository is strongest as a broad map of major books, commentaries, reception files, adjacent disciplines, archaeology, linguistics, and gap audits. The most important missing layer is not simply “more titles.” It is bibliographic control, article-level debate mapping, primary-source infrastructure, and a repeatable method for deciding why an item belongs.

## Proposed top-level architecture

The repository should distinguish five kinds of files:

1. **Canonical/book files**: book-by-book guidance for Hebrew Bible/Old Testament, Apocrypha/Deuterocanon, New Testament, and related corpora.
2. **Evidence files**: primary texts, critical editions, manuscripts, inscriptions, papyri, archaeological objects, datasets, images, coins, seals, maps.
3. **Method files**: textual criticism, philology, history, literary methods, social-scientific methods, reception, anthropology, critical theory, digital humanities, pedagogy.
4. **Subfield files**: Second Temple Judaism, rabbinics, Christian origins, patristics, Islam/Qur'an, reception history, global interpretation.
5. **Discovery/maintenance files**: journals, indexes, series, search protocols, metadata schema, and quality-control checklist.

The expansion files supplied here are designed to fill categories 2, 3, 4, and 5, and to enrich category 1 through `03-book-by-book-article-matrix.md`.

## Standard entry template

Every major topic, biblical book, corpus, or method should eventually be normalized under the following headings:

```markdown
## Topic or Book

### Scope
What the section covers and what it excludes.

### Primary evidence
Critical editions, manuscript corpora, inscriptional/papyrological evidence, archaeological data, translations, images, maps, datasets.

### Reference infrastructure
Lexica, grammars, concordances, encyclopedias, handbooks, indexes, bibliographic databases, review journals.

### Classic scholarship
Major monographs and article/chapter landmarks that still define the conversation.

### Article-level debate clusters
Named debates, journals where those debates occur, representative articles/chapters, and search strings for ongoing updates.

### Current state-of-the-question
Recent handbooks, review essays, introductions, special issues, or conference volumes.

### Critical/global approaches
Feminist, womanist, Black, Latinx, Asian, African, Indigenous, queer, disability, ecological, trauma, postcolonial, decolonial, class, empire, and other lenses relevant to this topic.

### Reception and lived use
Jewish, Christian, Islamic, secular, artistic, musical, liturgical, political, legal, devotional, pedagogical, and popular receptions.

### Non-English scholarship
German, French, Italian, Spanish, Portuguese, Dutch, Scandinavian, Hebrew, Arabic, Syriac, Greek, Russian, Chinese, Korean, Japanese, African-language, and Latin American scholarship as relevant.

### Quality notes
Superseded works, unstable terminology, confessional constraints, colonial assumptions, provenance risks, disputed dating, and evidentiary warnings.
```

## Citation and metadata schema

Each item should carry enough metadata to be useful outside a prose list. Use the following fields when converting entries to BibTeX, CSL JSON, CSV, Zotero, or a website:

| Field | Required? | Notes |
|---|---:|---|
| `author_editor` | Required | Use full names where known. |
| `title` | Required | Exact title, checked against publisher, journal, library catalog, or DOI metadata. |
| `type` | Required | Primary edition, monograph, article, chapter, review essay, database, corpus, journal, series, dissertation, encyclopedia entry, map, object catalogue. |
| `year` | Required when known | Use first publication date and revision/edition date where relevant. |
| `venue` | Required for articles/chapters | Journal, edited volume, series, database, archive, museum, excavation report. |
| `subfield` | Required | Hebrew Bible, NT, Qumran, Rabbinics, LXX, archaeology, etc. |
| `topic_tags` | Required | Controlled tags such as `textual-criticism`, `source-criticism`, `gender`, `empire`, `material-culture`. |
| `corpus_tags` | Optional | MT, SP, LXX, DSS, Targum, Peshitta, Vetus Latina, Coptic, etc. |
| `language` | Required | Language of scholarship or primary source. |
| `geography` | Optional | Region or scholarly tradition: German, Israeli, French, Latin American, Korean, African, etc. |
| `evidence_type` | Required | Literary, manuscript, inscriptional, papyrological, archaeological, iconographic, ethnographic, digital, oral, liturgical. |
| `period` | Optional | Iron Age, Persian, Hellenistic, Roman, late antique, medieval, early modern, modern, contemporary. |
| `status` | Required | Classic, current, superseded, contested, data tool, primary control, teaching resource. |
| `confidence` | Required | High, medium, low. Low means the entry must be verified before production use. |
| `notes` | Optional | Why it matters; limitations; where to look next. |

## Article-level policy

A serious biblical-studies bibliography should not rely on monographs and commentaries alone. Each topic should include at least four article-level layers:

1. **Landmark articles**: classic articles or chapters that created, redirected, or named a debate.
2. **State-of-the-question essays**: handbook chapters, review essays, or annual review-style pieces that summarize a debate.
3. **Recent debate clusters**: journal special issues, SBL session collections, edited volumes, or back-and-forth article clusters from the last 10-15 years.
4. **Database search protocols**: reproducible search strings for ATLA/Atla Religion Database, Old Testament Abstracts, New Testament Abstracts, RAMBI, L'Année philologique, Index Theologicus, Index Religiosus, International Medieval Bibliography, JSTOR, Project MUSE, Brill, De Gruyter, Oxford Academic, Cambridge Core, Peeters, Mohr Siebeck, Vandenhoeck & Ruprecht, SBL Press, and relevant open corpora.

## Recommended repository changes

### Add a root index

Create a top-level `README.md` or `index.md` with these categories:

```markdown
# Biblical Scholarship Research Ecosystem

## Core biblical books
- per-book.md
- per-book-supplement.md
- 03-book-by-book-article-matrix.md

## Discovery infrastructure
- 01-journals-indexes-series.md
- data/search_protocols.yml
- data/article_seed.csv

## Primary evidence and critical editions
- 06-versional-textual-criticism.md
- 07-primary-corpora-critical-editions.md
- 08-material-culture-digital-ethics.md

## Subfields
- 04-historical-jesus-synoptic-problem.md
- 05-rabbinics.md
- 10-early-judaism-qumran-second-temple.md
- 11-early-christianity-apocrypha-patristics.md
- 12-islam-quran-late-antique-scriptures.md

## Method and reception
- 09-global-critical-interpretation.md
- 13-reception-liturgy-lived-religion.md
- 14-linguistics-philology-translation.md
- 15-pedagogy-public-scholarship.md

## Governance
- 16-quality-control-maintenance.md
```

### Add item tags

Use tags to make lists machine-readable:

- `#primary-edition`
- `#database`
- `#journal`
- `#series`
- `#article-landmark`
- `#article-current`
- `#state-of-question`
- `#review-essay`
- `#non-english`
- `#global-critical`
- `#textual-criticism`
- `#material-culture`
- `#provenance-risk`
- `#superseded-but-important`
- `#teaching`

### Add confidence levels

Use one of:

- `verified`: checked against publisher, DOI, library catalogue, or official project site.
- `standard`: widely recognized work; metadata should still be checked before export.
- `seed`: useful lead, but bibliographic details must be verified.
- `debate-marker`: not a final bibliographic item; marks a debate that requires database harvesting.

## Coverage audit workflow

Run a coverage audit at least annually:

1. For each biblical book and major subfield, count primary editions, secondary monographs, articles, review essays, journals, non-English items, global-critical items, reception items, and material-culture items.
2. Check whether at least three major non-Anglophone scholarly traditions are represented where relevant.
3. Check whether the most important journals for the subfield are represented.
4. Search recent SBL, EABS, IOSOT, SNTS, AAR, ASOR, AOS, AJS, NAPH, and patristics/medieval conference programs for recurring themes not yet represented.
5. Mark every gap as one of: missing field, missing evidence type, missing language tradition, missing method, missing period, missing geography, missing primary corpus, missing article-level debate.
6. Convert accepted additions to structured metadata.

## Minimum expert-satisfaction threshold

For a topic to look like a research ecosystem to field specialists, it should have:

- At least one primary-text or evidence-control section.
- At least one index/database route for finding articles.
- At least five journals or series where the topic is actively published.
- At least ten article/chapter-level leads, unless the topic is narrow.
- At least three non-Anglophone or non-US/UK traditions where applicable.
- Explicit treatment of method and evidentiary limits.
- A reception/lived-use route when the topic has later cultural life.
- An ethics/provenance note when artifacts, manuscripts, antiquities, or human communities are involved.

