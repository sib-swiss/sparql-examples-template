# SPARQL examples template repository

This is a template repository to help you get started with sharing your sparql examples in a structured maner.


The idea comes from the [SIB SPARQL Examples](https://github.com/sib-swiss/sparql-examples/) project. 

# Upon forking

Change YOUR\_PROJECT to what you need it to be, adapt the index.md files.
Add your prefixes.ttl and examples in \*.ttl files.
Correct the LICSENSE.md and CITATION.cff to account for your project.


# For more inspiration see

 * [SIB Sparql Examples](https://github.com/sib-swiss/sparql-examples/)
 * [Wikibase Examples](https://github.com/JervenBolleman/wikibase-sparql-examples/)
 * [BiGCAT-UM](https://github.com/BiGCAT-UM/sparql-examples)

# The QA and markdown 

Can be found in the project [SIB SPARQL Examples Utils](https://github.com/sib-swiss/sparql-examples-utils/)

# How to test github page rendering locally

```sh
docker build -t sparql-examples-template .
docker run --rm -v "$PWD":/srv/jekyll sparql-examples-template bundler exec jekyll build --watch &
python3 -m http.server 8792 --directory _site
```
Build a local docker image that has the right Jekyll version and use that to build the webpages.
Then serve that with the python3 inbuild basic http server.
Open a browser locally at `http://localhost:8792/` to see the rendered HTML.

