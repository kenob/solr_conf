solr_conf
=========

This repository currently holds the solr files for indexing news articles from the NYC news corpus.

<h3>Basic Setup</h3>
- Install solr as described <a href="http://lucene.apache.org/solr/4_2_1/tutorial.html">here</a>
- Navigate to example folder in the directory of your solr installation
- Delete the solr folder
- Clone this repository, and rename the resulting folder to "solr"

<h3>Corpus-Specific Setup </h3>
<h5> NYC Corpus </h5>
- Create a folder 
- Download all tgz files from the NYC_* folder on ublearns, and place them in a folder
- Extract the tgz files
- Change the baseDir property on line 10 of newsArticleCollection/data-config.xml to the <strong>ABSOLUTE</strong> path of the folder created above

<h3> Usage </h3>
- Run the solr admin panel, navigate to the newsArticleCollection core, and execute a dataImport
- Search with an empty query(q = \*:\*), and you should get some results.

