# Templates for IS

-   Describe how to develop templates (important for word reference documents: modify the pandoc template instead of including other word documents)
```
docker run --rm --volume "`pwd`:/data" --user `id -u`:`id -g` pandoc_dockerfile -o reference.docx --print-default-data-file reference.docx > reference.docx
```
-   Mention the position of templates in the manuscript production process
-   Describe things to consider when using the templates (general and template-specific checklists)
-   For conferences: replace the templates from previous years

# Overview

## ECIS

-   [Manuscript template](ECIS2021.docx)
-   [CSL for references](...)
-   [Author guidelines](styles/apa-6th-edition-no-ampersand.csl)
-   Notes:
    - Manually update: Heading style for abstract and reference should be "subtitle"
    - APA 6 (no ampersand) seems to fit best. Manual changes necessary:
      - Journal titles: add quotes
      - Proceedings: capitalize
      - volume/issue: add space
      - Editors (e.g., in proceedings)
-   Status: Developmental

## ICIS

-   [Manuscript template](todo)
-   [CSL for references](...)
-   [Author guidelines](...)
-   Notes:-
-   Status: Developmental

## Information and Management

-   [Manuscript template](APA-7.docx)
-   [CSL for references](styles/elsevier-with-titles.csl)
-   [Author guidelines](https://www.elsevier.com/journals/information-and-management/0378-7206/guide-for-authors)
-   Notes:
  - No strict formatting requirements
  - Bibliography should use journal abbreviations (described [here](bibliography-journal-abbreviations.md)): abbreviations-ltwa.json
-   Status: Developmental

## Journal of the Association for Information Systems

-   [Manuscript template](APA-7.docx)
-   [CSL for references](...)
-   [Author guidelines](https://aisel.aisnet.org/jais/authorinfo.html)
-   Notes:-
-   Status: Developmental

## Information Systems Research

-   [Manuscript template](ISR.docx)
-   [CSL for references](styles/institute-for-operations-research-and-the-management-sciences.csl)
-   [Author guidelines](https://pubsonline.informs.org/page/isre/submission-guidelines), [Latex style files](https://pubsonline.informs.org/authorportal/latex-style-files), [Style guide](https://pubsonline.informs.org/pb-assets/INFORMS_style_guide-1.6-1574695301483.pdf)
-   Notes:
    - Booktitles need to be abbreviated manually (conference proceedings)
-   Bibliography should use journal abbreviations (described [here](bibliography-journal-abbreviations.md)): abbreviations-informs.json
-   Status: Developmental

## Organizational Research Methods

-   [Manuscript template](APA-7.docx)
-   [CSL for references](styles/apa-6th-edition.csl)
-   [Author guidelines](https://journals.sagepub.com/author-instructions/ORM)
-   Notes:-
-   Status: Developmental

## MIS Quarterly

-   [Manuscript template](MISQ.docx)
-   [CSL for references](styles/mis-quarterly.csl)
-   [Author instructions](https://misq.org/instructions/)
-   Notes:
    - Remove authors (title page and document properties) for review.
    - Include keywords on page 1.
    - Copy paper title to page 2.
    - Fix manually: Third Subhead: On same line as beginning of text, flush left, bold, upper/lower case, followed by a colon.
-   Status: Developmental

## Journal of Information Technology

-   [Manuscript template](MISQ.docx)
-   [CSL for references](styles/sage-harvard.csl)
-   [Author instructions](https://journals.sagepub.com/author-instructions/JIN#ManuscriptPrep)
- Notes:
    - There is no need to follow a specific template when submitting your manuscript in Word. However, please ensure your heading levels are clear, and the sections clearly defined.
-   Status: Developmental

# Additional resources

Searching CSL by example: https://csl.mendeley.com/searchByExample/
Word reference document, heading numbers: https://www.layoutheo.de/tutorials/ueberschriften/ueberschriften-nummerieren-blog.html

[rticles](https://github.com/rstudio/rticles)
[oxforddown](https://github.com/ulyngs/oxforddown)
[papaja](https://github.com/crsh/papaja)
