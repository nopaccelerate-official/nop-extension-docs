If you want to delete data from the Solr Index then you just need to simply run a single query in browser.

http://<hostname>:<port>/<solr-app-name>/<core-name>update?stream.body=<delete><query>*:*</query></delete>&commit=true

Let us see an example:

Suppose, I have a core with name **"Solr_sample"** and my solr server is running on **port 8983**, then the query will be:

http://localhost:8983/solr/Solr_sample/**update?stream.body=<delete><query>*:*</query></delete>&commit=true**

![Test1](../assets/img/Delete_Data.png)

[← Previous](ReloadCore.md) | [Next →](StartSolronSystemStartup.md)