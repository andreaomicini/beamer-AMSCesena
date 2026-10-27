# beamer-AMSCesena

> A simple Beamer-LaTeX style for presentations by Alma Mater Studiorum —
> Università di Bologna, in the blues of CesenaSMA2006, the first style of the
> series, recovered

## author

* Andrea Omicini

## usage

```latex
\documentclass[presentation]{beamer}\mode<presentation>{\usetheme{AMSCesena}}
```

Everything else is AMSUniBo's: the `apice` option for the APICe BibTeX field,
the `bologna` and `cesena` options for the seal watermark — none unless asked
for — and the commands and the bibliography style. The old styles
always carried the Campus di Cesena seal, so a deck moved from them wants
`cesena`:

```latex
\documentclass[presentation,cesena,apice]{beamer}\mode<presentation>{\usetheme{AMSCesena}}
```

A ready-to-use presentation skeleton is available in
[beamer-AMSCesena-template](https://github.com/andreaomicini/beamer-AMSCesena-template).

## relation to beamer-AMSUniBo and to CesenaSMA2006

This style is [beamer-AMSUniBo](https://github.com/andreaomicini/beamer-AMSUniBo)
with a different palette, exactly as
[beamer-AMSBolognaFC](https://github.com/andreaomicini/beamer-AMSBolognaFC) is:
the theme is AMSUniBo's, generated from it with every colour name replaced and
a handful of assignments changed where a role needed a different shade. The
options, the commands (`\speaker`, `\ccite`, `\uurl`, `\ddoi`, `\apicepubpar`,
`\apicetalkpar`, `\apicethesispar`, `\aalert`, the APICe addresses `\apice`,
`\apicesite`, `\apicepage`, and their pairs), the workarounds, the references
frame and `apalike-AMS.bst` — AMSUniBo 1.7.3's, with talks, theses and
subtitles — are all AMSUniBo's: see
[its README](https://github.com/andreaomicini/beamer-AMSUniBo#readme) for all of
them. The faces are not: like AMSBolognaFC, this style keeps LaTeX's own
Computer Modern, as the old one did, rather than AMSUniBo's Merriweather.

The palette is the one thing that is not, and it is a **recovery**.
`CesenaSMA2006` (October 2006, for the course *Sistemi Multi-Agente LS* in
Cesena) was the first Beamer style of the series: Beamer's `smoothbars` and
`infolines` outer themes merged into one, the `rounded` inner theme with
shadows, and the `orchid` and `whale` colour themes over Beamer's default blue.
It defined no colour of its own. Every later style descends from it: the
yearly course copies (`CesenaSMA2007`–`2009`, `CesenaSD2008`–`2010`,
`CesenaLTI2007`), then `AMSCesena` (2010–2013), whose reds and greys are
[beamer-AMSRedGrey](https://github.com/andreaomicini/beamer-AMSRedGrey)'s,
and the others after it.

The name is the series' first, with no qualifier, because the style is the
first. It is not the 2010 `AMSCesena`: that theme, red over `beaver`'s greys,
survives as the orphan branch `cesena` of beamer-AMSRedGrey, tag
`cesena-1.0`, and still declares `\usetheme{AMSCesena}` there. The two never
meet, since a deck reaches its style only through its own `.style` submodule.
The colour theme is called `orchidwhale`, after the two it comes from, and not
`cesena`, which is already the seal option.

The colours were computed from the old theme's Beamer mixes and checked against
the pixels of the 2006 PDFs. They were then assigned to the roles AMSUniBo's
palette has. Where a role had no counterpart in the old style, the colour was
guessed, and the colour theme says so beside it.

## structure

<!-- markdownlint-disable MD013 -->
| file | what it is |
| --- | --- |
| `beamerthemeAMSCesena.sty` | the theme: AMSUniBo's, in this palette |
| `beamercolorthemeorchidwhale.sty` | the palette alone, with the provenance of each colour, loaded by the theme |
| `almabologna-background.pdf` | the background under the `bologna` option: the Ateneo seal, as in AMSUniBo |
| `almacesena-background.pdf` | the same, with the Campus di Cesena seal, for the `cesena` option |
| `apalike-AMS.bst` | the bibliography style, AMSUniBo's |

<!-- markdownlint-enable MD013 -->

Every release attaches a `style.zip` holding all five plus the `LICENSE`.

## the palette

**Blue is the identity colour**: the title box, author, links, bullets.
**Deep blue is the structural one**: block headers, emphasis, the table of
contents. The head and foot lines are whale's black over its blues, as in 2006.
Unlike AMSUniBo and AMSRedGrey, **alerts are not the identity colour**: they
stay Beamer's red, as they were in 2006, and examples Beamer's green.

<!-- markdownlint-disable MD013 -->
| colour | value | source | where it goes on a slide |
| --- | --- | --- | --- |
| `owblue` | `#3333B2` | beamer@blendedblue, the 2006 structure | title box, author, bullets, links, DOIs, date in the foot line |
| `owbluedeep` | `#262686` | structure!75!black, whale secondary, orchid block title | block headers, emphasis, section in TOC, sub-section and title in head/foot, the APICe marker |
| `owbluedark` | `#1A1A59` | structure!50!black, whale tertiary | palette tertiary |
| `owbluelight` | `#C2C2E8` | structure!30!white, guessed: the light blue | separation lines |
| `owbluetint` | `#E9E9F3` | orchid block body | block bodies |
| `owbluepale` | `#EBEBF7` | structure!10, whale sidebar primary | sidebar |
| `owbluemid` | `#9999D9` | structure!50, whale sidebar tertiary | sidebar |
| `owred` | `#FF0000` | red, Beamer's alerted text | alerted text |
| `owreddeep` | `#BF0000` | red!75!black, orchid alerted block title | alerted block headers |
| `owredfill` | `#F9E6E6` | orchid alerted block body | alerted block bodies |
| `owgreen` | `#008000` | green!50!black, Beamer's example text | example text |
| `owgreendeep` | `#006000` | example text!75!black, orchid example block title | example block headers |
| `owgreenfill` | `#E6EFE6` | orchid example block body | example block bodies |
| `owblack` | `#000000` | black, whale quaternary | section in head/foot, author in head/foot |
| `owtext` | `#000000` | black, Beamer's normal text | body text |
| `owgrey` | `#404040` | darkgray, guessed: institute | institute |
| `owgreymid` | `#5A5A5A` | gray!70!black, guessed: secondary text | secondary text, footnotes, subtitle, date |
| `owgreyline` | `#BFBFBF` | lightgray, guessed: \ccite, \uuurl | `\ccite`, `\uuurl`, `\dddoi`, `\aalert`, fine rules |
| `owgreybg` | `#ECECEC` | gray!15!white, guessed: \cccite | `\cccite`, the lightest of the pair |

<!-- markdownlint-enable MD013 -->

White on `owblue` is 9.30:1, on `owbluedeep` 12.32:1, on `owreddeep` 6.53:1 and
on `owgreendeep` 7.86:1, so every block header and band carries white text;
`owblue` on white is 9.30:1 and on the block body 7.72:1. **The one pair below
WCAG AA is the 2006 alert**: `owred` on white is 4.00:1, and 3.32:1 on a block
body. It is kept as it was, since it is the original red; a deck that needs AA
there can redefine `alerted text`. The quiet light-on-dark commands are as in
AMSUniBo: `\ccite` (`owgreyline`) is 6.70:1 on a block header but 3.55:1 on the
alerted one, where `\cccite` (`owgreybg`) reaches 5.53:1, so on an `alertblock`
header prefer `\cccite`.

## versioning

The style version is declared in `beamerthemeAMSCesena.sty` as
`\stylemajor` / `\styleminor` / `\stylepatch`, giving `Major.Minor[.Patch]`.
`\stylepatch` is optional: comment it out to release as `Major.Minor`.

Releases are tagged `Major.Minor[.Patch]-<UTC time-stamp>`, with the time-stamp
appended automatically by the CI at release time.

## licence

This work is distributed under the
[LaTeX Project Public License](LICENSE), version 1.3c or later, and has the
LPPL maintenance status `maintained`.

One file is **not** covered by that licence: `apalike-AMS.bst` is a modified,
renamed derivative of Oren Patashnik's `apalike.bst` (Copyright © 1988, 2010
Oren Patashnik) and remains subject to its own terms, which permit modification
and redistribution provided the resulting file is renamed — as it is here.
