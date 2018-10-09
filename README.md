### Autotuning under Tight Budget Constraints: a Transparent Design of Experiments Approach

This paper was written and exported to `pdf` using [Emacs Org mode](https://orgmode.org/).

#### Org Mode LaTex: Exporting IEEEtran

After installing the IEEEtran template, add the following to your `Emacs`
configuration to be able to export using the `org-ieeetran` class:

```lisp
(with-eval-after-load 'ox-latex
  (add-to-list 'org-latex-classes
                '("org-ieeetran"
                  "\\documentclass{IEEEtran}"
                  ("\\section{%s}" . "\\section*{%s}")
                  ("\\subsection{%s}" . "\\subsection*{%s}")
                  ("\\subsubsection{%s}" . "\\subsubsection*{%s}")
                  ("\\paragraph{%s}" . "\\paragraph*{%s}")
                  ("\\subparagraph{%s}" . "\\subparagraph*{%s}"))))
```

You must use the `pdflatex` compiler to generate the correct template in `pdf`. You can
use `latexmk` in your `Emacs` configuration to properly export references:

```lisp
(setq org-latex-pdf-process (list "latexmk -pdflatex='pdflatex' -pdf -f %f"))
```
