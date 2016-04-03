Asciidoctor Lightweight Docker Image
==== 

Content
----

Based on Alpine, the image provides :

* Asciidoctor
* Aciidoctor Diagram with blockdiag and graphviz, 
* Asciidoctor PDF
* CodeRay and Pygments (source code highlighting)
* Asciidoctor backends

Build
----

    docker build -f asciidoctor -t sewatech/asciidoctor .

Run
----

    docker run -it -v $PWD:/documents/ sewatech/asciidoctor

Use
----

HTML with diagram

    asciidoctor -r asciidoctor-diagram sample-with-diagram.adoc

PDF with diagram

    asciidoctor-pdf -r asciidoctor-diagram sample-with-diagram.adoc
