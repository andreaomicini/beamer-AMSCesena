# beamer-AMSCesena — branch `cesena`

The **CesenaSMA2006** Beamer style, exactly as it sits beside the decks of the
course *Sistemi Multi-Agente LS*, A.Y. 2006/2007, in Cesena: the first Beamer
style of the series, the ancestor whose blues `main` recovered. It is not
`main` and never merges into it.

It exists so that the 2006/2007 course decks can be rebuilt as they were,
pinned through their `.style` submodule at the tag `cesena-2006`. Source:
`~/Documents/corsi/2005-2010/2006:2007/SMA-LS/slides/`, recovered on
2026-10-27; the commit carries the theme's own date, 2006-10-08.

Two files, both byte for byte:

* `beamerthemeCesenaSMA2006.sty` (2006/10/08): Beamer's `rounded` inner theme
  with shadows and the `orchid` and `whale` colour themes, over Beamer's default
  blue, with `\setbeamercovered{transparent}`; ten archive folders hold it,
  all identical. Its RCS header is Tantau's
  template line, kept by every later copy of the series.
* `beamerouterthemesmoothbarsinfolines.sty` (2006/10/07): Beamer's `smoothbars`
  outer theme of 2004 (RCS 1.5), with its head line, frame title and an
  `infolines`-like foot line declared under the name `smoothbarsinfolines
  theme`. The same file is in sixteen archive folders, all identical: it also
  served `Leuven2006` and `ICTTN2007`.

Neither loads an image: the UniBo logo in the corner of the 2006 slides is the
decks' own `\logo`, from their `img/`. The bibliography style of the time was
LaTeX's own `apalike`, not `apalike-AMS`.

The name `AMSCesena` of this repository is not the 2010 `AMSCesena`, the red
theme over `beaver`, which survives as the branch `cesena` of
[beamer-AMSRedGrey](https://github.com/andreaomicini/beamer-AMSRedGrey), tag
`cesena-1.0`.
