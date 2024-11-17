---
layout: default
title: Slurs and ties 
nav_order: 14
parent: "Features"
---

## Slurs and ties

Slurs are encoded with `slur`, and ties with `tie`, both using `@startid` and `@endid`.

The placement of the slurs or ties is encoded with `@curvedir`, and the style with `@lform`.

Relevant tests:
{% include test file="slur-01" %}
{% include test file="slur-02" %}
{% include test file="tie-01" %}

Known limitations:

* There is no distinction in the export between dashed and wide-dashed slur and both are exported with `@lform="dashed"`.
