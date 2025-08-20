# STIX 2.1 Errata 01 - Draft

The STIX 2.1 specification is provided with in asciidoc and markdown format.

Specification development in asciidoc or markdown has multiple advantages over editing the document in an online graphical editor.
* transparency - every document change is publicly visible as a git commit.
* ease of maintenance - style changes and changes to common text can be quickly and automatically made rather than editing each instance individually by hand.
* ease of validation - link checkers and other tools can be automated to ensure document currrency. Code examples can be held externally to document so that they can be validated by the stix-validator automatically, so that errors don't creep into the documented examples.
* ease of use - commonly consumed values, such as vocabulary overviews can be held in included documents and consumed directly rather than extracted from the document.

## AsciiDoctor

Generate HTML
```bash
asciidoctor  -v --failure-level INFO -a stylesheet=stix.css stix-v2.1.1.adoc
```

## Markdown

Generate HTML
```bash
pandoc -f gfm+definition_lists -t html  stix-v2.1.md --columns=345 --css css/stix.css --css css/page_override.css --embed-resources --standalone -o stix-v2.1.html
```
