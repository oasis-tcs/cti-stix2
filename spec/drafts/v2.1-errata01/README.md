# EXPERIMENTAL DRAFT

This is the STIX specification in asciidoc format. This is an experiment and *IS NOT* an official version of the STIX specification.

Specification development in asciidoc has multiple advantages over editing the document in an online graphical editor.
* transparency - every document change is publicly visible as a git commit.
* ease of maintenance - style changes and changes to common text can be quickly and automatically made rather than editing each instance individually by hand.
* ease of validation - link checkers and other tools can be automated to ensure document currrency. Code examples can be held externally to document so that they can be validated by the stix-validator automatically, so that errors don't creep into the documented examples.
* ease of use - commonly consumed values, such as vocabulary overviews can be held in included documents and consumed directly rather than extracted from the document.

Generate HTML
```bash
asciidoctor  -v --failure-level INFO -a stylesheet=stix.css stix-v2.1.1.adoc
```

Generate DocBook
```bash
asciidoctor  -b docbook -v --failure-level INFO -a stylesheet=stix.css stix-v2.1.1.adoc
```

Generate docx
```bash
pandoc -r docbook -t docx -o temp-v2.1.1.docx stix-v2.1.1.xml
```
Open the coversheet and import the temp-v2.1.1.docx file.
(Insert, Object, Text from File)
