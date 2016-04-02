FROM alpine

MAINTAINER Alexis Hassler <alexis.hassler@sewatech.fr> 

ENV BACKENDS_DIR /asciidoctor-backends 
ENV ASCIIDOCTOR_VERSION "1.5.4"

RUN apk add --no-cache ruby ruby-dev ruby-nokogiri
RUN apk add --no-cache bash build-base curl

RUN gem install --no-ri --no-rdoc asciidoctor
RUN gem install --no-ri --no-rdoc asciidoctor-diagram 
RUN gem install --no-ri --no-rdoc asciidoctor-pdf --version 1.5.0.alpha.11 
RUN gem install --no-ri --no-rdoc asciidoctor-epub3 --version 1.5.0.alpha.6
RUN gem install --no-ri --no-rdoc asciidoctor-confluence
RUN gem install --no-ri --no-rdoc coderay pygments.rb thread_safe 
RUN gem install --no-ri --no-rdoc slim 
RUN gem install --no-ri --no-rdoc haml tilt 
RUN curl -LkSs https://api.github.com/repos/asciidoctor/asciidoctor-backends/tarball | tar xfz - && mv /asciidoctor-asciidoctor-backend* $BACKENDS_DIR

CMD ["/bin/sh"]

