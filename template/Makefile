.PHONY: all clean show

OS=$(shell uname -s)
ifeq ($(OS),Linux)
  OPEN=xdg-open
endif
ifeq ($(OS),Darwin)
  OPEN=open
endif

DOCGEN=/usr/bin/env asciidoctor
SOURCES=$(wildcard docs/*.asciidoc)
TARGETS=$(SOURCES:.asciidoc=.html)

all: build $(TARGETS)
	mv build/docs/* build
	rm -rf build/docs

build:
	mkdir -p build

%.html: %.asciidoc
	$(DOCGEN) $< -o build/$@

show: build
	$(OPEN) build/index.html

clean:
	rm -rf build **/*~
