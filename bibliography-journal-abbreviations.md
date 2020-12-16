# Bibliography: journal abbreviations

## abbreviations-ltwa.json

-   Status: not complete (check reference section and add missing to json)
-   journal abbreviations according to [LTWA](https://www.issn.org/services/online-services/access-to-the-ltwa)
-   e.g., Information & Management (Elsevier), Information Systems Research (INFORMS)
    Makefile include:


    PANDOC_LATEX_OPTIONS = --pdf-engine=xelatex --citation-abbreviations=templates/abbreviations-ltwa.json
    PANDOC_DOCX_OPTIONS = --citation-abbreviations=templates/abbreviations-ltwa.json
    # Note: works only if the csl specifies form="short"
    # https://github.com/jgm/pandoc-citeproc/pull/254/commits/5fbe68f821f1b1afed179c0d7a925373ea65f8d6
