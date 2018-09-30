#### Autotuning under Budget Constraints: a Design of Experiments Approach

This paper was written and exported to `pdf` using [Emacs Org mode](https://orgmode.org/).

##### Org Mode LaTex: Exporting IEEEtran

Add the following to your `Emacs` configuration to be able to export using the
`org-ieeetran` class:

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
