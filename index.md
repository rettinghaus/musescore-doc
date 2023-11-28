---
title: Home
layout: home
nav_order: 1
---

[MEI](https://music-encoding.org) support in MuseScore stated through a collaboration between the [Digital and Cognitive Musicology Lab (DCML)](https://github.com/DCMLab) at the École polytechnique fédérale de Lausanne (EPFL) and the [Répertoire international des sources musicales (RISM) Digital Center](https://rism.digital) in Bern, Switzerland.

## Motivation

One of the main areas of research within the DCML is corpus studies, using large amounts of encoded notation. They maintain a large number of encodings entered using MuseScore, but are using the MEI format in their analysis and publishing toolchain. The current workflow of exporting to MusicXML and then converting to MEI has resulted in a number of problems in the quality of their analysis data, due in some part to ambiguities in the MusicXML format itself. A direct export to MEI from MuseScore will resolve these issues.

This is not the first attempt at supporting MEI in MuseScore. Members of the MEI community met with MuseScore developers in 2011, and again in 2013, where there was some support by the MuseScore development team but predicated on the MEI community providing funding for developing the software. Despite several efforts, including an unsuccessful Google Summer of Code application in 2021, this funding was not available. In the spring of 2023 some funding was made available through the DCML, and the project was launched as a partnership between the RISM Digital Center and DCML.

## MEI Basic

The goal is to provide "round trip" import and export of MEI from MuseScore. We are targeting the "MEI Basic" form of MEI, so called because it has been designed by the MEI community as a smaller, more limited subset of the larger MEI specification. MEI Basic is targeted at implementers of notation software for the purposes of supporting notation interchange. MEI v5, released in summer 2023, is the version of MEI that is read and written by MuseScore.