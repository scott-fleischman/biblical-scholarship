# 16. Quality Control, Metadata, and Maintenance

## Purpose

This file turns the bibliography into a maintainable scholarly project. It defines evidence standards, metadata fields, review procedures, and coverage audits. Without this governance layer, a large bibliography can become impressive but unreliable.

## Classification levels

Every entry should be classified by type:

| Type | Definition | Example |
|---|---|---|
| `primary-edition` | Critical edition or diplomatic edition of a primary text. | BHQ, Göttingen LXX, DJD, CSEL. |
| `primary-source` | Ancient, medieval, early modern, or modern reception artifact. | Mishnah, Josephus, sermon, film, inscription. |
| `database` | Searchable corpus, catalogue, or index. | Atla, RAMBI, Papyri.info, ORACC. |
| `journal` | Periodical venue. | JBL, VT, NTS, DSD. |
| `series` | Monograph/commentary/edition series. | Hermeneia, STDJ, BZAW. |
| `commentary` | Commentary on biblical or related text. | ICC, Hermeneia, Anchor Yale. |
| `monograph` | Single-author or edited scholarly book. | Topic-specific book. |
| `article` | Journal article. | Landmark or current article. |
| `chapter` | Essay in edited volume, handbook, Festschrift, conference proceedings. | State-of-question chapter. |
| `review-essay` | Extended review or bibliographic review. | RBL, Currents in Biblical Research. |
| `dissertation` | Doctoral dissertation or thesis. | Use sparingly; include institution. |
| `public-scholarship` | Non-peer-reviewed but expert-facing public resource. | Bible Odyssey, Ancient Jew Review. |
| `teaching-resource` | Pedagogical resource. | Syllabus, module, OER. |
| `artifact` | Object, inscription, coin, manuscript, image, site, map. | Mesha Stele, P66, Qumran jar. |

## Status tags

Each item should carry one or more status tags:

- `classic`: historically foundational.
- `current`: still part of live scholarly debate.
- `state-of-question`: summarizes field status.
- `superseded`: replaced in data or method but historically important.
- `contested`: influential but significantly disputed.
- `introductory`: useful for orientation.
- `advanced`: assumes specialist background.
- `primary-control`: must be consulted before making claims.
- `method-control`: needed to avoid methodological error.
- `non-english`: scholarship not in English.
- `global-critical`: global, minoritized, or critical approach.
- `provenance-risk`: artifact/manuscript requires ethical caution.
- `public-facing`: designed for broad audiences.
- `teaching`: useful in classrooms.

## Evidence-type tags

Use consistent evidence tags:

- `literary`.
- `manuscript`.
- `textual-variant`.
- `versional`.
- `epigraphic`.
- `papyrological`.
- `numismatic`.
- `archaeological`.
- `iconographic`.
- `liturgical`.
- `musical`.
- `homiletic`.
- `ethnographic`.
- `legal`.
- `philosophical`.
- `digital-corpus`.
- `oral-performance`.
- `material-religion`.

## Corpus tags

- `MT`.
- `SP`.
- `LXX`.
- `DSS`.
- `Targum`.
- `Peshitta`.
- `Vetus-Latina`.
- `Vulgate`.
- `Coptic`.
- `Armenian`.
- `Georgian`.
- `Ethiopic`.
- `Arabic`.
- `Slavonic`.
- `NT-papyri`.
- `Patristic`.
- `Rabbinic`.
- `Qur'an`.

## Metadata template

```yaml
- id: short-stable-id
  author_editor: ""
  title: ""
  type: "article | monograph | primary-edition | database | ..."
  year: ""
  venue: ""
  publisher: ""
  series: ""
  volume_issue_pages: ""
  doi_or_url: ""
  language: ""
  subfield: ""
  topic_tags: []
  corpus_tags: []
  evidence_type: []
  period: ""
  geography: ""
  status_tags: []
  confidence: "verified | standard | seed | debate-marker"
  annotation: "Why this item matters."
  caution: "Superseded? contested? provenance issue? confessional? outdated?"
  verified_against: "publisher | DOI | library catalog | database | specialist review"
  date_checked: "YYYY-MM-DD"
```

## Review procedure for adding an item

1. **Identify need.** Which gap does the item fill: evidence, method, book, article debate, non-English, global-critical, reception, or current scholarship?
2. **Verify metadata.** Check publisher, DOI, library catalog, journal site, WorldCat, or database record.
3. **Classify type and status.** Use required tags.
4. **Annotate.** One sentence: why it matters.
5. **Add caution.** Note if superseded, contested, dated, confessional, or ethically sensitive.
6. **Cross-link.** Add to every relevant book/topic file.
7. **Review.** At least one field-aware reader should check specialist areas.

## Coverage audit checklist

For each biblical book or major topic, verify presence of:

| Layer | Required? | Notes |
|---|---:|---|
| Primary text/edition | Yes | Critical edition or corpus. |
| Manuscript/versional evidence | Yes where applicable | MT/LXX/DSS/SP/Targum/Peshitta/NT witnesses. |
| Lexica/grammars/tools | Yes where language matters | Avoid generic language claims. |
| Major commentaries | Yes | Already strong in existing repo. |
| Landmark monographs | Yes | Classic and current. |
| Landmark articles/chapters | Yes | Missing in many bibliographies. |
| State-of-question essays | Yes | Handbooks, review essays. |
| Journals/indexes | Yes | Where to update. |
| Non-English scholarship | Yes where applicable | Especially German, French, Hebrew, Italian, Spanish, Dutch. |
| Global-critical scholarship | Yes | Integrated, not appended. |
| Material culture | Where applicable | Archaeology, inscriptions, papyri, coins, images. |
| Reception/liturgy/lived use | Where applicable | Usually applicable. |
| Ethics/provenance | Where artifacts/manuscripts involved | Mandatory. |
| Teaching/public scholarship | Optional but recommended | Especially for controversial texts. |

## Field-specific minimum thresholds

### Hebrew Bible / Old Testament

- BHS/BHQ/HUBP status.
- LXX and DSS where relevant.
- ANE comparanda where relevant.
- At least five article/chapter leads per major book or corpus.
- German/French/Hebrew scholarship where applicable.
- Archaeology/epigraphy for historical claims.
- Critical/global approaches integrated.

### New Testament

- NA/UBS/ECM status.
- Manuscript and versional evidence for textual issues.
- Historical Jesus/Synoptic Problem for Gospels.
- Greco-Roman/Jewish context.
- Papyri/inscriptions/material culture for social claims.
- Paul within Judaism, empire, gender, race/ethnicity, slavery, economics.
- Anti-Judaism warnings for Gospels, Paul, Hebrews, Revelation.

### Rabbinics

- Tannaitic vs amoraic vs later layers separated.
- Palestinian vs Babylonian separated.
- Manuscripts and critical editions where possible.
- Hebrew scholarship included.
- Rabbinics not treated only as reception.

### Archaeology/material culture

- Final excavation reports preferred over popular summaries.
- Provenance required.
- Chronology debates named.
- Scientific methods and limitations noted.
- Nationalist/colonial interpretive histories flagged.

### Reception

- Primary reception artifacts included.
- Multiple communities represented.
- Harmful reception named.
- Art/music/liturgy/preaching/popular culture not reduced to elite commentary.

## Red flags

Mark entries or sections for review if they show:

- No article-level sources.
- Only Anglophone scholarship.
- Only Protestant/Catholic/Jewish/evangelical/European perspectives where the topic crosses communities.
- No primary evidence.
- No edition control.
- No ethics/provenance note for artifacts.
- Claims based on unprovenanced objects.
- Reliance on outdated encyclopedias without current scholarship.
- Theological claims presented as historical consensus.
- Historical claims without archaeology/epigraphy/papyrology where relevant.
- Rabbinic texts used anachronistically for the first century.
- “The Septuagint says” without book/version specificity.
- “The original text” used without defining textual-critical goal.

## Pull request template

```markdown
## Proposed addition

Title / author / year:

## Type
- [ ] primary edition
- [ ] primary source
- [ ] article
- [ ] chapter
- [ ] monograph
- [ ] commentary
- [ ] database/index
- [ ] journal/series
- [ ] artifact/site/object
- [ ] public/teaching resource

## Subfield and topic tags

## Why it belongs

## Metadata verified against
- [ ] publisher
- [ ] DOI
- [ ] library catalog
- [ ] subject database
- [ ] specialist recommendation

## Status
- [ ] classic
- [ ] current
- [ ] state-of-question
- [ ] contested
- [ ] superseded but important
- [ ] primary-control
- [ ] method-control

## Gaps filled
- [ ] article-level
- [ ] non-English
- [ ] global-critical
- [ ] primary evidence
- [ ] material culture
- [ ] reception/lived religion
- [ ] textual/versional
- [ ] pedagogy/public scholarship

## Cautions

## Cross-links to update
```

## Annual maintenance cycle

### January-March

- Check new books and reviews from previous year.
- Update RBL and major journal review sections.
- Review new critical editions and database changes.

### April-June

- Search Atla, OTA, NTA, RAMBI, IxTheo, Index Islamicus, L'Année philologique for article updates.
- Add recent special issues and review essays.

### July-September

- Audit non-English and global-critical coverage.
- Invite specialist review for one underdeveloped file.

### October-December

- Review SBL, AAR, ASOR, AJS, EABS, IOSOT, SNTS, NAPH, patristics, and medieval conference programs for emerging debates.
- Create a “new debates” issue list.

## Suggested repository issues

Create GitHub issues with labels:

- `gap:article-level`
- `gap:non-english`
- `gap:global-critical`
- `gap:primary-evidence`
- `gap:textual-criticism`
- `gap:material-culture`
- `gap:reception`
- `gap:rabbinics`
- `gap:early-judaism`
- `gap:christian-origins`
- `gap:islam-quran`
- `gap:ethics`
- `needs:metadata-verification`
- `needs:specialist-review`
- `status:superseded`
- `status:contested`

## Expert review rota

A serious ecosystem should periodically recruit reviewers from:

- Hebrew Bible / Pentateuch.
- Hebrew Bible / Prophets.
- Hebrew Bible / Writings.
- Septuagint.
- Dead Sea Scrolls.
- Ancient Near East.
- Archaeology/epigraphy.
- New Testament Gospels/Historical Jesus.
- Pauline studies.
- NT textual criticism.
- Rabbinics.
- Early Christianity/patristics.
- Islam/Qur'an/late antiquity.
- Reception/liturgy.
- Feminist/womanist/queer/critical race/disability/ecological studies.
- Global biblical interpretation.
- Digital humanities.
- Pedagogy/public scholarship.

## Final quality standard

The bibliography should enable a user to move from a biblical book or topic to:

1. The controlling primary evidence.
2. The relevant critical editions and manuscripts.
3. The major commentaries and monographs.
4. The landmark article debates.
5. The current journals and indexes.
6. The main scholarly disagreements.
7. The global and critical approaches.
8. The reception and lived-practice record.
9. The digital tools and datasets.
10. The ethical constraints and evidentiary risks.

When all ten are visible, specialists are much more likely to view the project as a research ecosystem rather than a reading list.

