solr_conf
=========

This repository currently holds the solr files for indexing news articles from the NYC news corpus.

Use as follows:

- Install solr as described <a href="http://lucene.apache.org/solr/4_2_1/tutorial.html">here</a>
- Navigate to example folder in the directory of your solr installation
- Delete the solr folder
- Clone this repository, and rename the resulting folder to "solr"
- Run the solr admin panel, navigate to the newsArticleCollection core, and execute a dataImport
- Search with an empty query(q = *:*), and you should get some results.
