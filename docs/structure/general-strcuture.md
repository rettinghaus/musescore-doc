---
layout: default
title: Score structure
nav_order: 1
parent: "General structure"
---

## Score structure

The score structure is encoded in the top-level `scoreDef` that is the first child of `score`.

Since there is not direct mapping of  part structure from MuseScore within the MEI `scoreDef`, the part structure is preserved through `label` and `labelAbbr` within `staffGrp` or `staffDef` elements.

Bracket supported are `bracket`, `brace`, `bracketsq` and `line`.

Relevant tests:
* {% include test file="score-01" %}
* {% include test file="score-02" %}

Known limitations:
* Bar line spanning in MuseScore is defined on a staff level. In MEI, this is defined through `staffGrp@bar.thru`. The current implementation, the value for `@bar.thru` is determined by the spanning of the first staff, and only for the first level of nesting `staffGrp`. 