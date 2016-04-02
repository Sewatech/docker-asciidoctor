= Build

 docker build -f asciidoctor -t sewatech/asciidoctor .

= Run

 docker run -it -v $PWD:/documents/ sewatech/asciidoctor
