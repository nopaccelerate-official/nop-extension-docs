We are expecting that you have completed [Java Setup](JAVASetup.md) and [download Solr](SOLRSetup.md) on your machine.

To start the Solr Server, all you need is to run few commands on your command prompt. Assuming you have extracted the Solr folder to

**"C:\Solr"**

---

## 1. Open Command prompt and execute below commands

[Note: You can also start solr on system startup, please check [steps here](StartSolronSystemStartup.md).]

a) select the location of bin folder of c:/ > solr > bin

![Test](../img/cmd.png)

b) You can start Solr using command : **solr start -p 8983**, Once your solr is started you can move forward for [Creating New Core](CreateCore.md)

Here, -p specifies the port number on which your solr server will run.

![Test1](../img/solrstart.png)

c) You can stop Solr using command : **solr stop -p 8983**

![Test2](../img/solrstop.png)

d) You can restart Solr using command : **solr restart -p 8983**

[← Previous](StartSolr.md) | [Next →](CreateCore.md)
