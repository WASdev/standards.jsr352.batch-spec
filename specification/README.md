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

I have been running the Java source examples through a pretty printer, and wrapping them with AsciiDoc app-listing macros.

    [[app-listing]]
    [source,java]
    ----
    // Java Code Goes Here...
    ----
