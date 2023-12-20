---
layout: default
title: XML IDs
nav_order: 2
parent: "General structure"
---

## XML IDs

Exporting to MEI from MuseScore generates MEI IDs (i.e., `@xml:id`s). These are used for internal referencing (e.g., the `@startid` on a `dynam` referencing the `chord` it is attached to), but they can also be used for referencing MEI elements externally.

The MEI IDs are randomly generated. This means that exporting a file twice will have different MEI IDs. However, it is possible to seed the random generator with a value to be given in a `xml:id` property in the MuseScore metatag properties. When exporting to MEI, the value in the metatag is set as the `@xml:id` of the root `mei` element. It is preserved at import too, meaning the the `mei@xml:id` is set as `xml:id` metatag property in the imported MuseScore file.

Some elements that do not have a corresponding MuseScore object have no `@xml:id`. These are:

* `accid`
* `beam`
* `gracegrp`
* `syl`
* `verse`

It is also the case for `scoreDef` and its content as well as `section`, `staff`, `layer`.

### Re-importing MEI data

When no `mei@xml:id` is given in the imported data, IDs in MEI data imported into MuseScore will be preserved, however only in memory and not in the MuseScore files. This means that they will be preserved only if the MEI file is re-exported straight away. All IDs will newly generated if the file is closed, re-open and then re-exported.

Modifying the data (e.g., changing the pitch of a note) will not modify the ID for the note. If some of the data is copied (e.g., the content of a measure), the copied data will be attribute new random IDs at export. 

If a `mei@xml:id` is given in the imported data, the value will be used to seed the random generator and IDs will be regenerated. Having modified the data (e.g., changed the pitch of a note) will not impact the MEI IDs, which will remain the same. However, if some elements are inserted or deleted, that will modify the IDs in the resulting MEI file.
