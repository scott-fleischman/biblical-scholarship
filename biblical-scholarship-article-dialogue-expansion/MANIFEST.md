# Manifest

This package is an add-on to the previous `biblical-scholarship-research-ecosystem` package.

## Counts

| Object | Count |
|---|---:|
| Dialogue nodes | 236 |
| Dialogue edges | 214 |
| Hot-topic backward traces | 15 |
| Recent article watchlist entries | 45 |
| Coverage-matrix rows | 14 |

## Files

- `README.md`
- `MANIFEST.md`
- `SOURCE_NOTES.md`
- `00-integration-and-method.md`
- `01-current-hot-topics-backward-traces.md`
- `02-dialogue-graph-field-guide.md`
- `03-pentateuch-law-dtrh-dialogues.md`
- `04-prophets-writings-wisdom-dialogues.md`
- `05-historical-jesus-synoptic-gospels-dialogues.md`
- `06-paul-john-revelation-dialogues.md`
- `07-textual-criticism-versional-manuscript-dialogues.md`
- `08-second-temple-qumran-rabbinics-dialogues.md`
- `09-critical-global-reception-dialogues.md`
- `10-archaeology-material-culture-provenance-dialogues.md`
- `11-quran-islam-late-antique-dialogues.md`
- `12-digital-computational-methods-dialogues.md`
- `13-harvesting-and-maintenance-playbook.md`
- `14-sbl-reviewer-article-dialogue-checklist.md`
- `15-dialogue-summary-statistics.md`
- `data/dialogue_nodes.csv`
- `data/dialogue_edges.csv`
- `data/hot_topic_traces.csv`
- `data/recent_article_watchlist.csv`
- `data/dialogue_coverage_matrix.csv`
- `data/edge_relation_legend.csv`
- `data/harvest_queries.yml`
- `appendices/field_specific_journal_harvest.md`
- `appendices/current_issue_watch_protocol.md`

## Data model

`dialogue_nodes.csv` stores works. `dialogue_edges.csv` stores directed relationships between works. In an edge, `source_node` is the later or active work and `target_node` is the earlier or interlocutor work.

Examples:

```text
may_1993 -> malbon_1985 | responds | Mark 2.15 house
goodacre_2002 -> kloppenborg_1987 | challenges | Q/Farrer
pippin_1992 -> sfiorenza_1985_revelation | critiques/radicalizes | Revelation/gender
press_2025 -> cross_dss_1958 | ethical corrective | DSS forgeries
```

## Limits

This is a research map, not a complete bibliography. It deliberately includes `needs-page-verification` entries. Those entries identify scholarly waypoints that should be checked in Atla, IxTheo, OTA/NTA, RAMBI, L’Année philologique, Project MUSE, JSTOR, Brill, Cambridge Core, SAGE, or library catalogues before formal citation.
