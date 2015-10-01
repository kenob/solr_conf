solr_conf
=========

This repository currently holds the solr files for indexing news articles from the NYC news corpus and wikipedia articles from wikimedia xml files

<h3>Basic Setup</h3>
- Install solr as described <a href="http://lucene.apache.org/solr/4_2_1/tutorial.html">here</a>
- Navigate to example folder in the directory of your solr installation
- Delete the solr folder
- Clone this repository, and rename the resulting folder to "solr"

<h3>Instance-Specific Setup </h3>
<h5> NY Times Corpus </h5>
- Create a folder 
- Download all tgz files from the NYT Corpus folder under projects on ublearns, and place them in a folder
- Extract the tgz files
- Change the newsDataDirectory property on line 10 of newsArticleCollection/core.properties to the <strong>ABSOLUTE</strong> path of the folder created above. No quotes are required, but for windows, you'll have to replace "\\" with "\\\"

<h5> Wikipedia Articles </h5>
- Download and extract wikipedia xml files [[TODO:place url here]] and put them in a folder
- Depeat the final step for NYC corpus above, replacing newsDataDirectory with wikiDataDirectory and newsArticleCollection with wikiArticleCollection

<h3> Usage </h3>

<h4>Indexing </h4>
- Run the solr admin panel, and execute a dataImport on either the newsArticleCollection or wikiArticleCollection core to index news articles and wikipedia articles respectively 

<h5>OR</h5>

- Navigate to the flask app base folder
- With your virtual environment activated, run the command "python run.py refresh_index <wiki or news>"

<h4> Searching </h4>
- Run queries on the solr admin panel
- To search in the flask web application, import and use either the search or get_item helper defined in app/utils.py as shown in app/views.py

