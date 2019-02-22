# designdoc

Simple tool for generating AsciiDoc plans and designs for software projects.

* [Example Design Document](https://etscrivner.github.io/designdoc/index.html)

## Philosophy

Disciplined software engineering practices encourage developers to create plans
and designs for everything they do - whether it be a modification/extension of
an existing project or an entirely new project.

The `designdoc` tool helps facilitate creating this documentation by offering
an opinionated default setup for documenting a new project. It relies on a
[Ruby](https://www.ruby-lang.org/en/) tool called [AsciiDoctor](https://asciidoctor.org/) for generating documentation from
[AsciiDoc](http://asciidoc.org/) markup. The documentation structure is shown below:

```
Project Root (docs/index.asciidoc)
├── Project Plan (docs/plan.asciidoc)
├── Project Design (docs/design.asciidoc)
```

A series of navigable webpages is generated from your documentation and can be
freely browsed and shared with colleagues for review. AsciiDoctor provides a
clean and readable default styling.

## Usage

**Generate New Documentation Project**

```
designdoc new /path/to/docfolder
```

**Build All Documentation**

From the root of the documentation folder you can build all documentation as follows:

```
make
```

**Open Documentation Root**

You can open the top-level HTML file for your generated documentation in your
default web browser as follows:

```
make show
```

**Remove All Built Files**

You can also clear out all of the built documentation files as follows:

```
make clean
```
