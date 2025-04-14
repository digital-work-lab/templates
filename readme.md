# Templates for IS

- Explain the position of templates in the manuscript production process

# Contributing

How to develop templates [1](https://bookdown.org/yihui/rmarkdown-cookbook/word-template.html ):

-   [ ] Describe things to consider when using the templates (general and template-specific checklists)
-  Important for word reference documents: modify the pandoc template instead of including other word documents)
```
docker run --rm --volume "`pwd`:/data" --user `id -u`:`id -g` pandoc_dockerfile -o reference.docx --print-default-data-file reference.docx > reference.docx
```
-   For conferences: replace the templates from previous years

# Basic Template

The [basic](basic.tex) template offers a simple Latex template for developing manuscripts before finalizing them with a custom journal/conference template.
Since this template does not include journal-specific layouts, all manuscripts are formatted consistently.
In addition, the template includes header information on the current version of the manuscript (based on the git history and the markdown header):

```
ShortTitle (YYYY-MM-DD, Committer, branch, commit-id)
```

Adding this information to the PDF allows you to easily find the version (git commit) that corresponds to the PDF.
This is particularly useful when printing PDFs or sharing them for feedback.

Using the [basic](basic.tex) template requires gitinfo2, which must be set up in the individual manuscript repositories:

```
cp /usr/share/texlive/texmf-dist/tex/latex/gitinfo2/post-xxx-sample.txt .git/hooks/post-checkout
cp .git/hooks/post-checkout .git/hooks/post-merge
cp .git/hooks/post-checkout .git/hooks/post-commit
```

It has to be installed in the pandoc-docker container as suggested in this [Dockerfile](Dockerfile).
To build the container, simply run:

```
docker build -t pandoc_dockerfile .
```


# Custom Journal/Conference Templates

## ECIS

-   [Manuscript template](ECIS2021.docx)
-   [CSL for references](custom-styles/ecis.csl)
-   [Author guidelines](...)
-   Notes:
    - Manually update: Heading style for abstract and reference should be "subtitle"
    - Manually update the short title (header)
    - Authors: should be in individual lines.
-   Status: Developmental

## ICIS

-   [Manuscript template](ICIS2021.docx)
-   [CSL for references](styles/mis-quarterly.csv)
-   [Author guidelines](...)
-   Notes:-
-   Status: Developmental

## Information and Management (I&M)

-   [Manuscript template](APA-7.docx)
-   [CSL for references](styles/elsevier-with-titles.csl)
-   [Author guidelines](https://www.elsevier.com/journals/information-and-management/0378-7206/guide-for-authors)
-   Notes:
  - No strict formatting requirements
  - Bibliography should use journal abbreviations (described [here](bibliography-journal-abbreviations.md)): abbreviations-ltwa.json
-   Status: Developmental

## Journal of the Association for Information Systems (JAIS)

-   [Manuscript template](APA-7.docx)
-   [CSL for references](...)
-   [Author guidelines](https://aisel.aisnet.org/jais/authorinfo.html)
-   Notes:-
-   Status: Developmental

## Information Systems Research (ISR)

-   [Manuscript template](ISR.docx)
-   [CSL for references](styles/institute-for-operations-research-and-the-management-sciences.csl)
-   [Author guidelines](https://pubsonline.informs.org/page/isre/submission-guidelines), [Latex style files](https://pubsonline.informs.org/authorportal/latex-style-files), [Style guide](https://pubsonline.informs.org/pb-assets/INFORMS_style_guide-1.6-1574695301483.pdf)
-   Notes:
    - Booktitles need to be abbreviated manually (conference proceedings)
-   Bibliography should use journal abbreviations (described [here](bibliography-journal-abbreviations.md)): abbreviations-informs.json
-   Status: Developmental

## Organizational Research Methods (ORM)

-   [Manuscript template](APA-7.docx)
-   [CSL for references](styles/apa.csl)
-   [Author guidelines](https://journals.sagepub.com/author-instructions/ORM)
-   Notes:-
-   Status: Developmental

## Communications of the Association for Information Systems (CAIS)

-   [Manuscript template](CAIS.docx)
-   [CSL for references](custom_styles/cais.csl) (APA without DOIs)
-   [Author guidelines](https://aisel.aisnet.org/cais/format.html)
-   Notes: Titles are automatically linked with DOIs (pandoc/citeproc built-in that cannot be deactivated) - the only solution is to remove / comment dois in bib-file.
-   Status: Developmental

## Journal of Information Systems Education (JISE)

-   [Manuscript template](JISE.docx)
-   [CSL for references](styles/jise.csl)
-   [Author guidelines](https://jise.org/initial.html)
-   Notes:-
-   Status: Developmental

## MIS Quarterly (MISQ)

-   [Manuscript template](MISQ.docx)
-   [CSL for references](styles/apa.csl)
-   [Author instructions](https://misq.org/instructions/)
-   Notes:
    - Remove authors (title page and document properties) for review.
    - Include keywords on page 1.
    - Copy paper title to page 2.
    - Fix manually: Third Subhead: On same line as beginning of text, flush left, bold, upper/lower case, followed by a colon.
    - Citation style changed to APA-7: https://misq.umn.edu/
-   Status: Developmental

## Journal of Information Technology (JIT)

-   [Manuscript template](MISQ.docx)
-   [CSL for references](styles/sage-harvard.csl)
-   [Author instructions](https://journals.sagepub.com/author-instructions/JIN#ManuscriptPrep)
- Notes:
    - There is no need to follow a specific template when submitting your manuscript in Word. However, please ensure your heading levels are clear, and the sections clearly defined.
-   Status: Developmental

# Additional resources

Searching CSL by example: https://csl.mendeley.com/searchByExample/
Word reference document, heading numbers: https://www.layoutheo.de/tutorials/ueberschriften/ueberschriften-nummerieren-blog.html
Particular styles (e.g., "Figure") in Word document may need to be activated/added to the catalogue before editing them in the reference document.

- [APA-Latex](https://github.com/mamadgit/APA-Custom-LaTeX-Template)
- [rticles](https://github.com/rstudio/rticles)
- [oxforddown](https://github.com/ulyngs/oxforddown)
- [papaja](https://github.com/crsh/papaja)
