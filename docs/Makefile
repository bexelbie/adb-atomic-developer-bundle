ifneq ($(COMMIT_ID),)
	DO_COMMIT_ID = '--commit=$(COMMIT_ID)'
endif

SHELL := /bin/bash

html:
	# asciidoctor can only put a single HTML output
	# chunked output is close per upstream
	asciidoctor -d book -a linkcss -a stylesheet=http://www.projectatomic.io/stylesheets/application.css index.adoc

plain-html:
	asciidoctor index.adoc

clean:
	find . -type f -name \*.html -exec rm -f {} \;
	find . -type f -name \*.pdf -exec rm -f {} \;
	find . -type f -name \*.epub -exec rm -f {} \;
	find . -type f -name \*.fo -exec rm -f {} \;
	find . -type f -name \*.xml -exec rm -f {} \;
	rm -fr output/
