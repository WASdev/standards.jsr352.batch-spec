# JSR 352 Specification 1.0a as AsciiDoc

## Overview
This folder contains the JSR-352 1.0a Specification in Ascii Doc format. The conversion was largely automated, with several 
manual passes and edits.

jsr352-1_0_a.asc is the main document, and includes the individual parts.

## Rendering
GitHub currently [renders includes as a document link](http://asciidoctor.org/news/2014/02/04/github-asciidoctor-0.1.4-upgrade-5-things-to-know/#3-swap-an-include-for-a-link) 
instead of palcing the include in-line... this makes it look terrible when viewed online! 

If you clone this repository and render the document using AsciiDocter, you'll get one comprehensive specification document, 
complete with table of contents.

## Outstanding Tasks

### Code Wrapping
I have been running the Java source examples through a pretty printer, and wrapping them with AsciiDoc app-listing macros. When I do each block, I run the code through a pretty-printer, so it appears consistent and clean.

    [[app-listing]]
    [source,java]
    ----
    // Java Code Goes Here...
    ----

XML code blocks can be wrapped similarly, and the JSL examples and snippets still need to be wrapped.

    [[app-listing]]
    [source,xml]
    ----
    <!-- XML Document Goes Here -->
    ----

### Verification Against the Spec

The conversion to AsciiDoc was largely automated, but some more complex sections of the specification needed to be reworked manually. This applies especially to the Job Runtime Lifecycle section (job_runtime_lifecycle.adoc). 

Each section should be carefully reviewed against the [the Maintenance Release Specification](https://jcp.org/aboutJava/communityprocess/mrel/jsr352/index.html)

### Psuedo Code Blocks

The subsections under job_runtime_lifecycle.adoc contain psuedo-code descriptions, which were represented as a nested-list 
structure in the original specification document. This didn't translate well into AsciiDoc. It looks bad in text, and renders slightly different than the original document.

I tried my best to ensure the nested levels all match, so it flows the same. But I would very much like to see these Psuedo Code elements re-written into a more readable form.
