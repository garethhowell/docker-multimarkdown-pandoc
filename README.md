# docker-multimarkdown-pandoc
A Docker container with the tools to run [MultiMarkdown](https://github.com/fletcher/MultiMarkdown-6) and [pandoc](https://pandoc.org/) as part of a document management system.

# Motivation
I use [Markdown](https://www.markdownguide.org/) to author a variety of documents that are used by my [Scout](https://scouts.org.uk) Group. 
These documents often share a lot in common with additional audience-specific content.
I used to use MS Word to author these documents, making use of the *Master Document* feature. 
However, after being burned yet again by its many bugs, I re-created all the documents as a series of Markdown files and now use
[MultiMarkdown](https://github.com/fletcher/MultiMarkdown-6) and [pandoc](https://pandoc.org/) to compile the documents into PDF files.
Docker container to permit "compiling" multimarkdown documents to multiple targets: e.g. PDF

# Acknowledgements
This container builds on the excellent work done by [Thomas Weise](https://github.com/thomasweise) in his many docker-related efforts, and starts from his [docker-pandoc](https://github.com/thomasweise/docker-pandoc) image.
