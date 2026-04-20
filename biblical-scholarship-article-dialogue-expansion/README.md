# Biblical Scholarship Article-Dialogue Expansion Pack

Created: 2026-04-19

This is a second add-on package for `scott-fleischman/biblical-scholarship`. It does not replace the earlier research-ecosystem expansion. It adds an article-dialogue layer: key articles, monographs used as debate waypoints, response chains, current hot-topic anchors, and backward genealogies.

## What this package adds

- `236` dialogue nodes in `data/dialogue_nodes.csv`
- `214` directed dialogue edges in `data/dialogue_edges.csv`
- `15` current-hot-topic backward traces in `data/hot_topic_traces.csv`
- `45` recent article watchlist entries in `data/recent_article_watchlist.csv`
- `14` subfield coverage rows in `data/dialogue_coverage_matrix.csv`
- Markdown field guides that convert the structured data into readable debate maps

## Design goal

The earlier expansion made the bibliography into a research ecosystem. This package adds the next layer: **scholarly conversation over time**.

For each major debate, the package asks:

1. What is the current hot article cluster?
2. What older articles or monographs does it depend on?
3. Which works directly respond to which?
4. What are the major changes of direction?
5. What search strings should be run next in Atla, OTA/NTA, IxTheo, RAMBI, L’Année philologique, JSTOR, Project MUSE, Brill, Cambridge Core, SAGE, and publisher platforms?

## How to integrate

Copy this directory into the repository as:

```text
article-dialogue-expansion/
```

Then add this line to the repository index or README:

```markdown
- [Article-dialogue expansion](article-dialogue-expansion/README.md): article-level debate chains, current hot-topic traces, and directed response maps.
```

## Recommended workflow

Use `data/dialogue_edges.csv` as the source of truth. Use the Markdown files for browsing. When adding a new article, add a node, then add at least one edge that says what it responds to, extends, challenges, revises, or reframes.
