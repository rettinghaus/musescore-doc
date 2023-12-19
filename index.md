---
title: Home
layout: home
nav_order: 1
---

# MEI support in MuseScore

[MEI](https://music-encoding.org) support in [MuseScore](https://musescore.org) (as of 4.2) started through a collaboration between the Digital and Cognitive Musicology Lab (DCML) at the Ecole polytechnique fédérale de Lausanne (EPFL) and the RISM Digital Center in Bern, Switzerland.

| [![DCML]({{ site.baseurl }}/assets/images/dcml.png)](https://github.com/DCMLab) | [![DCML]({{ site.baseurl }}/assets/images/rism-digital.png)](https://rism.digital) |

## Motivation

One of the main areas of research within the DCML is corpus studies, using large amounts of encoded notation. They maintain a large number of encodings entered in MuseScore, but are also using the MEI format in their analysis and publishing toolchain. The current workflow, which often imports MusicXML and then converts it to MEI or MuseScore, has impeded the growth of high-quality corpora, partly due to certain ambiguities within the MusicXML format itself. A direct conversion method between MEI and MuseScore will resolve these issues.

This is not the first attempt at supporting MEI in MuseScore. Members of the MEI community met with MuseScore developers in 2011, and again in 2013, where there was some support by the MuseScore development team but predicated on the MEI community providing funding for developing the software. Despite several efforts, including an unsuccessful Google Summer of Code application in 2021, this funding was not available. In the spring of 2023 some funding was made available through the DCML, and the project was launched as a partnership between the RISM Digital Center and DCML.

## MEI Basic

The support in MuseScore is targeting the "MEI Basic" form of MEI, so called because it has been designed by the MEI community as a smaller, more limited subset of the larger MEI specification. MEI Basic is targeted at implementers of notation software for the purposes of supporting notation interchange. MEI v5, released in summer 2023, is the version of MEI that is read and written by MuseScore.

## Implementation

The implementation is based on the concept of round-trip loss-less conversion. This means that, exporting a file to MEI from MuseScore, re-importing it in MuseScore and re-exporting it to MEI is expected to produce twice exactly the same MEI file. Of course, since not all features are supported in the MEI export and import, only the ones implemented are taken into account for the evaluation.

The MuseScore implementation includes a set of [MEI test units]({{ site.musescore_test }}) that are used for evaluating the round-trip conversion. The status of these tests is constantly monitored through the continuous integration (CI) infrastructure of MuseScore.

## About this documentation

This documentation provides some information about the current status of the MEI support in MuseScore referencing the test units integrated in the MuseScore repository. In order to offer a direct visual impression of what each test unit is about, a rendering of them as obtained with [Verovio](https://verovio.org) is included in the documentation. 

{: .warning }
Readers should keep in mind that the Verovio rendering is only to give an idea of the content of the test unit and that the rendering in MuseScore will never be exactly the same.

## Feedback, questions or issues?

Please feel free to contact us at [info@rism.digital](info@rism.digital) for any questions. If you have any issues when importing or exporting files and cannot find information in this documentation, you can also open an issue on our [fork of the MuseScore repository](https://github.com/rism-digital/MuseScore/issues).
