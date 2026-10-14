# CleanNotes LaTeX Template

A small LaTeX template for clean notes, reports and handouts. It provides
Palatino-style typography, coloured headings, a compact title block and six
ready-to-use box styles.

## Use the template

Copy these three files into your project:

```text
main.tex
preamble.tex
cleannotes.sty
```

Edit the document information in `preamble.tex` and write your document in
`main.tex`. Compile `main.tex` with pdfLaTeX. A recent TeX Live or MiKTeX
installation is sufficient.

The [example](example/example.pdf) is a visual guide to the available boxes
and commands. It is standalone and does not use `preamble.tex`.

## Boxes

All boxes use the same syntax:

```latex
\begin{accentbox}[Title][docblue]
  Your text, lists or equations.
\end{accentbox}
```

Available styles:

| Environment | Appearance |
| --- | --- |
| `accentbox` | Tinted background, coloured left border and inline title |
| `framedbox` | Thin outline and separate title bar |
| `numberedbox` | Tinted box with an automatic number |
| `cardbox` | Compact padding and a separate title |
| `solidbox` | Solid colour with white text |
| `splitbox` | Left heading with a right heading |

The optional arguments are `[Title][Colour][Extra tcolorbox options]`.
Available colours include `docblue`, `tiporange`, `alertred`, `leafgreen`,
`slategray` and `softgray`. Any named xcolor colour can also be used.

For a numbered box, put `\label{box:id}` immediately after the opening command
and refer to it with `\ref{box:id}`. See the example for custom box variants,
`steps`, `proof`, `\step` and `\reason`.

## Options

Change the package line in `preamble.tex` to select a language or layout:

```latex
\usepackage[dutch]{cleannotes}
\usepackage[onepager]{cleannotes}
```

Available options are `english`, `dutch`, `unnumbered` and `onepager`; they can
be combined.

## License

This template is released under the [MIT License](LICENSE).
