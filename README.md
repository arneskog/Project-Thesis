# LaTeX skeleton -- Force Closure Margin project thesis

Skeleton for the NTNU Cybernetics and Robotics project thesis on
object-aided locomotion for a snake robot (Force Closure margin for
path planning). Based on the department's `Rapportmal_prosjekt`
template (title page layout and NTNU logo reused).

## Structure

```
LaTeX_Skeleton/
  main.tex                   <- master file, compile this one
  references.bib             <- bibliography (biblatex/biber)
  Figurer/ntnulogo.pdf        <- NTNU logo used on the title page
  chapters/
    abstract.tex
    preface.tex
    introduction.tex
    background.tex
    theory.tex
    margin_force_closure.tex   <- core contribution: the metric itself
    implementation.tex         <- implementing the margin
    simulation.tex
    evaluation.tex
    conclusion.tex
  appendices/
    appendix_a.tex
```

Every chapter file starts with a `% TODO:` comment block outlining a
suggested structure for that chapter -- replace the comments and
section headings with your own content as you write.

## Compiling

This project uses **biblatex + biber** for references, so the
compile sequence is:

```
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

In Overleaf this happens automatically (Overleaf detects biblatex
and runs biber for you) -- just set the compiler to `pdflatex` if it
isn't already, and upload this whole folder as your project.

Locally with `latexmk` (recommended, handles the repeated runs for
you):

```
latexmk -pdf main.tex
```

## Title page

Edit the placeholders in `main.tex` (`\title{...}` and
`\author{...}`): your name, supervisor, department and course code.

## References

Two example entries in `references.bib` were guessed from filenames
in your `Literature/` and `Background/` folders (the Gravdahl 2025
and Nordal 2026 papers) -- every field is marked `TODO` and must be
checked against the actual PDFs before you cite them. Add your
remaining sources as you read them.
